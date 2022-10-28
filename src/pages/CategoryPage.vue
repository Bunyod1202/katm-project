<template>
  <div>
    <section class="hero">
      <div class="container">
        <div class="hero__box">
          <div class="hero__start">
            <ul class="hero__list">
              <li class="hero__item">
                <p class="hero__text">
                  Тип кредитного отчёта:
                  <strong class="hero__span">
                    {{ non }}
                  </strong>
                </p>
              </li>
              <li class="hero__item">
                <p class="hero__text">
                  Тип субъекта кредитной информации:
                  <strong class="hero__span"> <!-- Заёмщик -->nane </strong>
                </p>
              </li>
              <li class="hero__item">
                <p class="hero__text">
                  Пользователь кредитного отчёта:
                  <strong class="hero__span">
                    <!-- Тошкент ш., АТ Халқ банкининг Яккасарой филиали (00824), Инагамов А.Б. -->nane
                  </strong>
                </p>
              </li>
              <li class="hero__item">
                <span class="hero__span-box">
                  <span class="hero__text">
                    Номер запроса:
                    <strong class="hero__span">
                      <!-- 0352 0191 4483 6101 -->nane
                    </strong>
                    Время запроса:
                    <strong class="hero__span">
                      {{ non }}
                    </strong>
                  </span>
                </span>
              </li>
              <li class="hero__item">
                <span class="hero__span-box">
                  <span class="hero__text">
                    Номер согласия:
                    <strong class="hero__span">
                      {{ non }}
                    </strong>
                    Дата согласия:
                    <strong class="hero__span">
                      {{ non }}
                    </strong>
                  </span>
                </span>
              </li>
              <li class="hero__item">
                <span class="hero__span-box">
                  <span class="hero__text">
                    Номер заявки:
                    <strong class="hero__span"> <!-- 134567 -->nane </strong>
                    Дата заявки:
                    <strong class="hero__span">
                      <!-- 2020-11-05 -->nane
                    </strong>
                  </span>
                </span>
              </li>
            </ul>
          </div>

          <img
            class="hero__left"
            src="/images/qrcode.png"
            width="100"
            height="100"
            alt="qrcode"
          />
        </div>
      </div>
    </section>

    <section class="info">
      <div class="container">
        <div class="info__title">
          <p class="info__title-text">1. СУБЪЕКТ КРЕДИТНОЙ ИНФОРМАЦИИ</p>
        </div>
        <div class="info__box">
          <div class="info__box-in">
            <img
              class="info__img"
              src="/images/human.png"
              width="150"
              height="200"
              alt="template"
            />

            <ul class="info__list">
              <li class="info__item">
                <span class="info__item-left">
                  Наименование (ГЦП):
                  <strong class="info__item-right">
                    {{ infoScore.client.name }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  ПИНФЛ (ГЦП):
                  <strong class="info__item-right">
                    {{ infoScore.client.pinfl }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Дата рождения (ГЦП):<strong class="info__item-right">
                    {{ infoScore.client.birth_date }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Пол (ГЦП):<strong class="info__item-right">
                    {{ infoScore.client.gender }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Юридический статус (КО):<strong class="info__item-right">
                    {{ non }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Адрес по прописке (МВД):<strong class="info__item-right">
                    {{ infoScore.client.address }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Адрес проживания (КО):<strong class="info__item-right">
                    {{ non }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Номер телефона (КО):<strong class="info__item-right">
                    {{ non }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Электронная почта (ЛК):<strong class="info__item-right">
                    {{ non }}
                  </strong>
                </span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title">
          <p class="info__title-text">2. ДОХОДЫ ПО ИНПС</p>
        </div>
        <div class="dogovor">
          <table>
            <thead>
              <tr>
                <th class="number">№</th>
                <th class="ws">ГОД И МЕСЯЦ НАЧИСЛЕНИЯ</th>
                <th class="ww">НАИМЕНОВАНИЕ ИСТОЧНИКА ДОХОДА</th>
                <th>ИНН ИСТОЧНИКА ДОХОДА</th>
                <th>ДАТА ОБНОВЛЕНИЯ</th>
                <th>СУММА ИНПС</th>
                <th>СУММА ДОХОДА</th>
              </tr>
            </thead>
            <tbody class="rosws">
              <tr
                class="rosw"
                v-for="(item, index) in infoScore.incomes.INCOME"
                :key="index"
              >
                <td class="number">{{ ++index }}</td>
                <td class="ws">{{ item.PERIOD }}</td>
                <td class="ww">{{ item.ORGNAME }}</td>
                <td>{{ item.ORG_INN }}</td>
                <td>n{{ non }}</td>
                <td>{{ item.INCOME_SUMMA }}</td>
                <td>n{{ non }}</td>
              </tr>
            </tbody>
            <tfoot>
              <tr class="rosw">
                <td class="number"></td>
                <td class="ws" colspan="2">
                  Итого за период с 2019-11-05 до 2020-10-05
                </td>
                <td class="ww"></td>
                <td></td>
                <td></td>
                <td></td>
              </tr>
            </tfoot>
          </table>
          <div class="info__title">
            <p class="info__title-text">
              3. НАЛИЧИЕ КРЕДИТНЫХ ОТЧЁТОВ О СУБЪЕКТЕ В КРЕДИТНОМ БЮРО
            </p>
          </div>
          <table>
            <thead>
              <tr>
                <th class="number">№</th>
                <th class="ww">КРЕДИТОР</th>
                <th>№ ДОГОВОРА</th>
                <th>ВАЛЮТА</th>
                <th>ОСТАТОК ВСЕЙ ЗАДОЛЖЕННОСТИ</th>
                <th>ПРОСРОЧЕННАЯ ЧАСТЬ</th>
                <th>СРЕДНЕМЕСЯЧНЫЙ ПЛАТЁЖ</th>
              </tr>
            </thead>
            <tbody class="rosws">
              <tr class="rosw">
                <td class="number">{{ non }}</td>
                <td class="ww">
                  {{ non }}
                </td>
                <td>{{ non }}</td>
                <td>non</td>
                <td>{{ non }}</td>
                <td>non</td>
                <td>non</td>
              </tr>
            </tbody>
            <tfoot>
              <tr class="rosw">
                <td class="number"></td>
                <td class="ww">Итого</td>
                <td></td>
                <td></td>
                <td></td>
                <td></td>
                <td></td>
              </tr>
            </tfoot>
          </table>
          <div class="info__title grin">
            <p class="info__title-text">4. ПРИМЕЧАНИЯ</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { useI18n } from "vue-i18n";

let infoScore = {
  incomes: {
    INCOME: [
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "1",
        PERIOD: "2021-08",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 11418000,
        NUM: "2",
        PERIOD: "2021-08",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "3",
        PERIOD: "2021-09",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 19029120,
        NUM: "4",
        PERIOD: "2021-09",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 9514560,
        NUM: "5",
        PERIOD: "2021-10",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "6",
        PERIOD: "2021-10",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4838346,
        NUM: "7",
        PERIOD: "2021-11",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 9514560,
        NUM: "8",
        PERIOD: "2021-11",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 9514560,
        NUM: "9",
        PERIOD: "2021-12",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "10",
        PERIOD: "2021-12",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "11",
        PERIOD: "2022-01",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 19029120,
        NUM: "12",
        PERIOD: "2022-01",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 24225520,
        NUM: "13",
        PERIOD: "2022-02",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "14",
        PERIOD: "2022-02",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "15",
        PERIOD: "2022-03",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 14551882,
        NUM: "16",
        PERIOD: "2022-03",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "17",
        PERIOD: "2022-04",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 14710960,
        NUM: "18",
        PERIOD: "2022-04",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 14710960,
        NUM: "19",
        PERIOD: "2022-05",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "20",
        PERIOD: "2022-05",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "21",
        PERIOD: "2022-06",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 14710960,
        NUM: "22",
        PERIOD: "2022-06",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "202042939",
        INCOME_SUMMA: 14710960,
        NUM: "23",
        PERIOD: "2022-07",
        ORGNAME: "Ягона умумреспублика проссесинг маркази",
      },
      {
        ORG_INN: "303032661",
        INCOME_SUMMA: 4752000,
        NUM: "24",
        PERIOD: "2022-07",
        ORGNAME: "SEIDE INTERNATIONAL MCHJ XK",
      },
    ],
  },
  incomes_period: {
    incomes_period_begin: "2021-08-24",
    incomes_period_end: "2022-08-24",
    incomes_all_summa: 232751508,
  },
  sysinfo: {
    Date: "2022-08-24 12:51:03",
    Bank: "TAQSIM SARMOYA",
    id_demand: "RET2022236743337",
    user_id: "System S. S.",
    claim_id: "2c9b9105d5ed4855a03e",
    report_name: "Заработная плата по ИНПС (XML)",
    Declaration:
      'Внимание! Предоставление и использование кредитной информации регулируется Законом Республики Узбекистан "Об обмене кредитной информацией" № 301 от 04.10.2011 года.',
    Branch: "20176",
    claim_date: "2022-08-24",
    report_code: "025",
  },
  presence_report: null,
  client: {
    pinfl: "33103940270022",
    address: "adres",
    document_number: "1637173",
    gender: "М",
    document_type_id: 6,
    birth_date: "1994-03-31",
    name: "Sultanbayev Sherzod Sarvar O‘G‘Li",
    inn: "-",
    document_date: "2013-05-28",
    resident: "Резидент",
    document_type: "Биометрический паспорт гражданина Республики Узбекистан",
    document_serial: "AA",
  },
  Notification: null,
};
</script>
<style lang="scss" scoped></style>
