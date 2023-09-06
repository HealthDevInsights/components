<script setup>

import { ref } from "vue";

const prescricaoOculos = ref ({
    esfericoDireitoLonge: 0,
    cilindricoDireitoLonge: 0,
    eixoDireitoLonge: 0,
    dnpDireitoLonge: 0,
    esfericoEsquerdoLonge: 0,
    cilindricoEsquerdoLonge: 0,
    eixoEsquerdoLonge: 0,
    dnpEsquerdoLonge: 0,
    adicao: 0,
    esfericoDireitoPerto: 0,
    cilindricoDireitoPerto: 0,
    eixoDireitoPerto: 0,
    dnpDireitoPerto: 0,
    esfericoEsquerdoPerto: 0,
    cilindricoEsquerdoPerto: 0,
    eixoEsquerdoPerto: 0,
    dnpEsquerdoPerto: 0,
    observacoes: '',
});

</script>

<template>
    <v-table fixed-header>
        <thead>
        <tr>
            <th>
                Para Longe
            </th>
            <th>

            </th>
            <th>

            </th>
            <th>

            </th>
            <th>

            </th>
        </tr>
        </thead>
        <tbody>
        <tr>
            <td>
                Olho direito
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.esfericoDireitoLonge"
                    type="number"
                    label="Esferico"
                    outlined
                    step="0.25"
                    min="-30"
                    max="20"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.cilindricoDireitoLonge"
                    label="Cilindrico"
                    type="number"
                    outlined
                    step="0.25"
                    max="0"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.eixoDireitoLonge"
                    type="number"
                    label="Eixo"
                    outlined
                    step="5"
                    min="0"
                    max="180"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.dnpDireitoLonge"
                    type="number"
                    label="DNP"
                    outlined
                    step="1"
                    min="20"
                    max="40"
                    suffix="mm"
                />
            </td>
        </tr>
        <tr>
            <td>
                Olho esquerdo
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.esfericoEsquerdoLonge"
                    type="number"
                    label="Esferico"
                    outlined
                    step="0.25"
                    min="-30"
                    max="20"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.cilindricoEsquerdoLonge"
                    type="number"
                    label="Cilindrico"
                    outlined
                    step="0.25"
                    max="0"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.eixoEsquerdoLonge"
                    type="number"
                    outlined
                    step="5"
                    min="0"
                    max="180"
                    label="Eixo"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.dnpEsquerdoLonge"
                    type="number"
                    outlined
                    step="1"
                    min="20"
                    max="40"
                    label="DNP"
                    suffix="mm"
                />
            </td>
        </tr>
        <tr>
            <td>
                Adição
            </td>
            <td>
                v
                <v-select
                    v-model="prescricaoOculos.adicao"
                    :items="[0.00, 0.25, 0.50, 0.75, 1.00, 1.25, 1.50, 1.75, 2.00, 2.25, 2.50, 2.75, 3.00]"
                    outlined
                    @change="alert = false"
                />

            </td>
        </tr>
        <tr>
            <td>
                Olho direito
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.esfericoDireitoPerto"
                    type="number"
                    outlined
                    step="0.25"
                    min="-30"
                    max="20"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.cilindricoDireitoPerto"
                    label="Cilindrico"
                    type="number"
                    outlined
                    step="0.25"
                    max="0"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.eixoDireitoPerto"
                    type="number"
                    outlined
                    step="5"
                    min="0"
                    max="180"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.dnpDireitoPerto"
                    type="number"
                    outlined
                    step="1"
                    min="20"
                    max="40"
                    suffix="mm"
                />
            </td>
        </tr>
        <tr>
            <td>
                Olho esquerdo
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.esfericoEsquerdoPerto"
                    type="number"
                    outlined
                    step="0.25"
                    min="0"
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.cilindricoEsquerdoPerto"
                    type="number"
                    outlined
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.eixoEsquerdoPerto"
                    type="number"
                    outlined
                />
            </td>
            <td>
                <v-text-field
                    v-model="prescricaoOculos.dnpEsquerdoPerto"
                    type="number"
                    outlined
                />
            </td>
        </tr>
        <tr>
            <td>
                Observações
            </td>
            <td colspan="4">
                <v-text-field
                    type="text"
                    v-model="prescricaoOculos.observacoes"
                    outlined
                />
                {{prescricaoOculos}}
            </td>
        </tr>
        </tbody>
    </v-table>
</template>

<style scoped>

</style>
