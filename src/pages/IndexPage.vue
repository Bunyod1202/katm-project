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
                    {{ infoScore.client.juridical_status }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Адрес по прописке (МВД):<strong class="info__item-right">
                    {{ infoScore.client.registration_address }}
                  </strong>
                </span>
              </li>
              <li class="info__item">
                <span class="info__item-left">
                  Адрес проживания (КО):<strong class="info__item-right">
                    {{ infoScore.client.live_address }}
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
                    {{ infoScore.client.email }}
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
          <p class="info__title-text">2. СКОРИНГ КИАЦ</p>
        </div>
        <div class="scoring">
          <div class="texts">
            <ul class="listes">
              <li>
                <strong class="listes-item"
                  ><p>СКОРИНГОВЫЙ БАЛЛ:</p>
                  <span>{{ infoScore.scorring.scoring_grade }}</span></strong
                >
              </li>
              <li>
                <strong class="listes-item"
                  ><p>КЛАСС ОЦЕНКИ:</p>
                  <span>{{ infoScore.scorring.scoring_level }}</span></strong
                >
              </li>
              <li>
                <strong class="listes-item"
                  ><p>ВЕРСИЯ СКОРИНГА:</p>
                  <span>{{ infoScore.scorring.scoring_version }}</span></strong
                >
              </li>
            </ul>
          </div>
          <div class="img">
            <img src="/images/res.png" alt="" />
          </div>
          <div class="">
            <div class="boxses">
              <p class="clasic">{{ infoScore.scorring.scoring_class }}</p>
              <p class="text">{{ scoringTitle }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title">
          <p class="info__title-text">3. ОБЩИЙ ОБЗОР (ОТКРЫТЫЕ + ЗАКРЫТЫЕ)</p>
        </div>
        <div class="obraz">
          <ul class="list">
            <li class="list-item">
              <strong>{{ infoScore.overview.claims_qty }}</strong
              ><span>-</span><span class="text">заявки</span>
            </li>
            <li class="list-item">
              <strong>{{ infoScore.overview.contracts_qty }}</strong
              ><span>-</span><span class="text">договора</span>
            </li>
            <li class="list-item">
              <strong>{{
                infoScore.overview.contingent_liabilities_qty
              }}</strong
              ><span>-</span><span class="text">условные обязательства</span>
            </li>
            <li class="list-item">
              <strong>{{ infoScore.overview.credit_request_qty }}</strong
              ><span>-</span>
              <span class="text">запросы и подписки по субъекту КИ</span>
            </li>
            <li class="list-item">
              <strong>{{ infoScore.overview.average_monthly_payment }}</strong
              ><span>-</span
              ><span class="text">среднемесячный платёж (сумма)</span>
            </li>
          </ul>
          <ul class="list lists">
            <li class="list-item">
              <strong>{{ infoScore.overview.overdue_principal_qty }}</strong
              ><span>-</span
              ><span class="text"
                >количество просрочек основного долга (ОД)</span
              >
            </li>
            <li class="list-item">
              <strong>{{
                infoScore.overview.max_overdue_principal_days
              }}</strong
              ><span>-</span
              ><span class="text">максимальная просрочка ОД (дни) </span>
            </li>
            <li class="list-item">
              <strong>{{ infoScore.overview.max_overdue_principal_sum }}</strong
              ><span>-</span
              ><span class="text">максимальная просрочка ОД (сумма)</span>
            </li>
            <li class="list-item">
              <strong>{{
                infoScore.overview.max_uninter_overdue_percent_days
              }}</strong
              ><span>-</span>
              <span class="text">
                максимальная непрерывная просрочка % (дни)</span
              >
            </li>
            <li class="list-item">
              <strong>{{ infoScore.overview.total_overdue_percent_sum }}</strong
              ><span>-</span
              ><span class="text">всего просроченных % (сумма) </span>
            </li>
          </ul>
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title">
          <p class="info__title-text">4. ДЕЙСТВУЮЩИЕ ДОГОВОРА</p>
        </div>
        <div class="dogovor">
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
              <tr
                class="rosw"
                v-for="(item, index) in infoScore.open_contracts.open_contract"
                :key="index"
              >
                <td class="number">{{ ++index }}</td>
                <td class="ww">
                  {{ item.contract_id }}
                </td>
                <td>{{ item.currency }}</td>
                <td>non</td>
                <td>{{ item.overdue_debt_sum }}</td>
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
          <!-- <q-table
            :columns="columns"
            :rows="infoScore.open_contracts.open_contract"
            row-key="name"
            hide-bottom
          /> -->
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title mt">
          <p class="info__title-text">5. ЗАЯВКИ БЕЗ ДОГОВОРОВ</p>
        </div>
        <div class="dogovor">
          <table>
            <thead>
              <tr>
                <th class="number">№</th>
                <th class="ww">КРЕДИТОР</th>
                <th>№ ЗАЯВКИ</th>
                <th>ДАТА ЗАЯВКИ</th>
                <th>ВАЛЮТА</th>
                <th>СУММА ЗАЯВКИ</th>
                <th>КОД ПРИЧИНЫ ОТКЛОНЕНИЯ</th>
                <th>ДАТА ОТКЛОНЕНИЯ</th>
              </tr>
            </thead>
            <tbody>
              <tr
                class="rosw"
                v-for="(itm, index) in infoScore.claims_wo_contracts
                  .claim_wo_contract"
                :key="index"
              >
                <td class="number">{{ ++index }}</td>
                <td class="ww">
                  {{ itm.branch }}
                </td>
                <td>{{ itm.claim_id }}</td>
                <td class="itm-data">{{ itm.claim_date }}</td>
                <td>{{ itm.currency }}</td>
                <td>{{ itm.summa }}</td>
                <td>{{ itm.rejection_reason }}</td>
                <td>{{ itm.rejection_date }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title mt">
          <p class="info__title-text">6. ДОГОВОРА</p>
        </div>
        <div class="chaild-title">
          <div class="">
            <strong class="tex-white">6.1 КРЕДИТОР:</strong
            ><span>ТОШКЕНТ Ш. ТИФ МИЛЛИЙ БАНКИНИНГ УЧТЕПА ФИЛИАЛИ (00918)</span>
          </div>
          <div class="">
            <strong class="tex-white">ТИП:</strong>
            <span>БАНК</span>
          </div>
        </div>
        <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Статус договора:</span
              ><strong>{{
                infoScore.contracts.contract.contract_status
              }}</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Номер договора:</span
              ><strong>{{ infoScore.contracts.contract.contract_id }}</strong>
            </li>

            <li class="item">
              <span class="num">3.</span><span>Дата начала договора:</span
              ><strong></strong>{{ infoScore.contracts.contract.contract_date }}
            </li>

            <li class="item">
              <span class="num">4.</span><span>Дата окончания договора:</span
              ><strong>{{
                infoScore.contracts.contract.contract_end_date
              }}</strong>
            </li>

            <li class="item">
              <span class="num">5.</span><span>Номер и дата заявки:</span
              ><strong>{{ infoScore.contracts.contract.claim_id }} </strong>
            </li>

            <li class="item">
              <span class="num">6. </span
              ><span>Юридический статус субъекта КИ: </span
              ><strong>{{
                infoScore.contracts.contract.juridical_status
              }}</strong>
            </li>

            <li class="item">
              <span class="num">7.</span><span>Вид кредита:</span
              ><strong> {{ infoScore.contracts.contract.credit_type }}</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Валюта договора: </span
              ><strong>{{ infoScore.contracts.contract.currency }}</strong>
            </li>

            <li class="item">
              <span class="num">9.</span><span>Процентная ставка:</span
              ><strong>{{ infoScore.contracts.contract.percent }}</strong>
            </li>

            <li class="item">
              <span class="num">10.</span><span>Обеспечение: </span
              ><strong>{{
                infoScore.contracts.contract.percent_change
              }}</strong>
            </li>

            <li class="item">
              <span class="num">11.</span><span>Класс качества активов:</span
              ><strong
                >{{ infoScore.contracts.contract.class_asset_quality }}
              </strong>
            </li>

            <li class="item">
              <span class="num">12. </span
              ><span>Резерв на покрытие возможных убытков:</span
              ><strong>{{
                infoScore.contracts.contract.reserve_bal_sum
              }}</strong>
            </li>
          </ul>
          <ul class="list mr100">
            <li class="item">
              <span class="num">13.</span><span>Сумма договора:</span
              ><strong>{{ infoScore.contracts.contract.amount }}</strong>
            </li>

            <li class="item">
              <span class="num">14.</span><span>Выданная сумма:</span
              ><strong>{{ infoScore.contracts.contract.amount_issued }}</strong>
            </li>

            <li class="item">
              <span class="num">15.</span
              ><span>Остаток всей задолженности:</span><strong></strong
              >{{ infoScore.contracts.contract.total_debt_sum }}
            </li>

            <li class="item">
              <span class="num">16.</span><span>Срочная задолженность ОД:</span
              ><strong
                >{{ infoScore.contracts.contract.immediate_principal_sum }}
              </strong>
            </li>

            <li class="item">
              <span class="num">17.</span><span>Срочная задолженность %:</span
              ><strong
                >{{ infoScore.contracts.contract.immediate_percent_sum }}
              </strong>
            </li>

            <li class="item">
              <span class="num">18. </span
              ><span> Просроченная задолженность ОД: </span
              ><strong>{{
                infoScore.contracts.contract.overdue_principal_sum
              }}</strong>
            </li>

            <li class="item">
              <span class="num">19.</span
              ><span>Просроченная задолженность %:</span
              ><strong>
                {{ infoScore.contracts.contract.overdue_percent_sum }}</strong
              >
            </li>

            <li class="item">
              <span class="num">20.</span
              ><span>Пересмотренная задолженность ОД: </span
              ><strong>{{
                infoScore.contracts.contract.revised_principal_sum
              }}</strong>
            </li>

            <li class="item">
              <span class="num">21.</span><span>Судебная задолженность ОД:</span
              ><strong>{{
                infoScore.contracts.contract.lawsuit_principal_sum
              }}</strong>
            </li>

            <li class="item">
              <span class="num">22.</span
              ><span>Внебалансовая задолженность ОД: </span
              ><strong>{{
                infoScore.contracts.contract.offbalance_princial_sum
              }}</strong>
            </li>

            <li class="item">
              <span class="num">23.</span
              ><span>Внебалансовая задолженность %:</span
              ><strong>{{
                infoScore.contracts.contract.offbalance_percent_sum
              }}</strong>
            </li>
          </ul>
        </div>
        <div class="contents">
          <p>Обеспечение - 1</p>
        </div>
        <!-- <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Тип обеспечения:</span
              ><strong>Поручитель</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Вид обеспечения:</span
              ><strong> Страховой полис</strong>
            </li>

            <li class="item">
              <span class="num">3.</span><span>Наименование:</span
              ><strong></strong>OOO «АLKON»
            </li>

            <li class="item">
              <span class="num">4.</span><span>Юридический статус: </span
              ><strong>Юридическое лицо</strong>
            </li>

            <li class="item">
              <span class="num">5.</span><span>ИНН:</span
              ><strong>301 000 155</strong>
            </li>
          </ul>
          <ul class="list">
            <li class="item">
              <span class="num">6.</span><span>Сумма обеспечения:</span
              ><strong>33 750 000</strong>
            </li>

            <li class="item">
              <span class="num">7.</span
              ><span>Валюта договора обеспечения: </span
              ><strong> Узбекский сум (860)</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Номер договора обеспечения:</span
              ><strong></strong>4086
            </li>

            <li class="item">
              <span class="num">9.</span><span>Дата договора обеспечения: </span
              ><strong>2019-09-25</strong>
            </li>

            <li class="item">
              <span class="num">10.</span
              ><span>Согласия субъекта на получение кредитной истории:</span
              ><strong>4086, 2019-09-24</strong>
            </li>
          </ul>
        </div> -->
        <div class="contents">
          <p>Обеспечение - 2</p>
        </div>
        <!-- <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Тип обеспечения: </span
              ><strong>Залогодатель</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Вид обеспечения:</span
              ><strong> Автомобиль</strong>
            </li>

            <li class="item">
              <span class="num">3.</span><span>Наименование:</span
              ><strong>Qosimov Shuxratbek Abduraximovich</strong>
            </li>

            <li class="item">
              <span class="num">4.</span><span>Юридический статус: </span
              ><strong>Физическое лицо</strong>
            </li>

            <li class="item">
              <span class="num">5.</span><span>ПИНФЛ:</span
              ><strong>31103 8701 11349</strong>
            </li>
          </ul>
          <ul class="list">
            <li class="item">
              <span class="num">6.</span><span>Сумма обеспечения:</span
              ><strong>50 000 000</strong>
            </li>

            <li class="item">
              <span class="num">7.</span
              ><span>Валюта договора обеспечения: </span
              ><strong> Узбекский сум (860)</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Номер договора обеспечения:</span
              ><strong></strong>11
            </li>

            <li class="item">
              <span class="num">9.</span><span>Дата договора обеспечения: </span
              ><strong>2019-09-25</strong>
            </li>

            <li class="item">
              <span class="num">10.</span
              ><span>Согласия субъекта на получение кредитной истории:</span
              ><strong>11, 2020-09-24</strong>
            </li>
          </ul>
        </div> -->
        <div class="contents">
          <p>Прогнозный график платежей</p>
        </div>
        <!-- <div class="month">
          <table>
            <thead>
              <tr>
                <th></th>
                <th>ЯНВАРЬ</th>
                <th>ФЕВРАЛЬ</th>
                <th>МАРТ</th>
                <th>АПРЕЛЬ</th>
                <th>МАЙ</th>
                <th>ИЮНЬ</th>
                <th>ИЮЛЬ</th>
                <th>АВГУСТ</th>
                <th>СЕНТЯБРЬ</th>
                <th>ОКТЯБРЬ</th>
                <th>НОЯБРЬ</th>
                <th>ДЕКАБРЬ</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td class="brn">2019 г. ОД %</td>
                <td colspan="9" class="brn"></td>
                <td>
                  <p>0</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>0</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>0</p>
                  <p>1 500 000</p>
                </td>
              </tr>
              <tr>
                <td class="brn">2020 г. ОД %</td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
              </tr>
              <tr>
                <td class="brn">2019 г. ОД %</td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td>
                  <p>5 000 000</p>
                  <p>1 500 000</p>
                </td>
                <td colspan="9" class="brn"></td>
              </tr>
            </tbody>
          </table>
        </div> -->
        <div class="contents">
          <p>Фактическое погашение</p>
        </div>
        <!-- <div class="row">
          <div class="cols">
            <table class="tables">
              <thead class="dogovor theads">
                <tr>
                  <th class="wws">ДАТА</th>
                  <th>ПОГАШЕНИЕ ОД</th>
                  <th>ПОГАШЕНИЕ %</th>
                  <th>ОСТАТОК ОД</th>
                </tr>
              </thead>
              <tbody class="tbodys">
                <tr>
                  <td class="wws">2019-10-24</td>
                  <td></td>
                  <td>1 500 000</td>
                  <td>75 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2019-11-22</td>
                  <td></td>
                  <td>1 500 000</td>
                  <td>75 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2019-12-24</td>
                  <td></td>
                  <td>1 500 000</td>
                  <td>75 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2020-01-22</td>
                  <td>5 000 000</td>
                  <td>1 500 000</td>
                  <td>70 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2020-02-24</td>
                  <td>5 000 000</td>
                  <td>1 500 000</td>
                  <td>65 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2020-03-24</td>
                  <td>3 000 000</td>
                  <td>1 500 000</td>
                  <td>62 000 000</td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="col">
            <table class="tables">
              <thead class="dogovor theads">
                <tr>
                  <th class="wws">ДАТА</th>
                  <th>ПОГАШЕНИЕ ОД</th>
                  <th>ПОГАШЕНИЕ %</th>
                  <th>ОСТАТОК ОД</th>
                </tr>
              </thead>
              <tbody class="tbodys">
                <tr>
                  <td class="wws">2019-10-24</td>
                  <td></td>
                  <td>1 500 000</td>
                  <td>75 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2019-11-22</td>
                  <td></td>
                  <td>1 500 000</td>
                  <td>75 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2019-12-24</td>
                  <td></td>
                  <td>1 500 000</td>
                  <td>75 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2020-01-22</td>
                  <td>5 000 000</td>
                  <td>1 500 000</td>
                  <td>70 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2020-02-24</td>
                  <td>5 000 000</td>
                  <td>1 500 000</td>
                  <td>65 000 000</td>
                </tr>
                <tr>
                  <td class="wws">2020-03-24</td>
                  <td>3 000 000</td>
                  <td>1 500 000</td>
                  <td>62 000 000</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div> -->
        <div class="contents">
          <p>Просроченные платежи основного долга</p>
        </div>
        <!-- <div class="row">
          <div class="cols">
            <table class="tables">
              <thead class="dogovor theads">
                <tr>
                  <th class="wws">№</th>
                  <th>ДАТА ОБРАЗОВАНИЯ</th>
                  <th>ДНИ</th>
                  <th>СУММА</th>
                  <th>ДАТА ОБНОВЛЕНИЯ</th>
                </tr>
              </thead>
              <tbody class="tbodys">
                <tr>
                  <td class="wws">1</td>
                  <td>2020-03-26</td>
                  <td>3</td>
                  <td>2 000 000</td>
                  <td>[2020-03-29]</td>
                </tr>
              </tbody>
            </table>
          </div>
          <div class="col">
            <table class="tables">
              <thead class="dogovor theads">
                <tr>
                  <th class="wws">№</th>
                  <th>ДАТА ОБРАЗОВАНИЯ</th>
                  <th>ДНИ</th>
                  <th>СУММА</th>
                  <th>ДАТА ОБНОВЛЕНИЯ</th>
                </tr>
              </thead>
              <tbody class="tbodys">
                <tr>
                  <td class="wws">2</td>
                  <td>2020-09-26</td>
                  <td>9</td>
                  <td>5 000 000</td>
                  <td>[2020-09-26]</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div> -->
        <div class="chaild-title">
          <div class="">
            <strong class="tex-white">6.2 КРЕДИТОР:</strong
            ><span
              >ТОШКЕНТ Ш., «TENGE BANK» АКЦИЯДОРЛИК ТИЖОРАТ БАНКИ (01176)</span
            >
          </div>
          <div class="">
            <strong class="tex-white">ТИП:</strong>
            <span>БАНК</span>
          </div>
        </div>
        <!-- <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Статус договора: </span
              ><strong>: Закрыт (2020-03-05)</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Номер договора:</span
              ><strong> 6752</strong>
            </li>

            <li class="item">
              <span class="num">3.</span><span>Дата начала договора:</span
              ><strong>2019-03-10</strong>
            </li>

            <li class="item">
              <span class="num">4.</span><span>Дата окончания договора: </span
              ><strong>2020-03-08</strong>
            </li>

            <li class="item">
              <span class="num">5.</span><span>Номер и дата заявки:</span
              ><strong>70547, 2019-03-10</strong>
            </li>

            <li class="item">
              <span class="num">6.</span
              ><span>Юридический статус субъекта КИ:</span
              ><strong>Индивидуальный предприниматель</strong>
            </li>

            <li class="item">
              <span class="num">7.</span><span>Вид кредита:</span
              ><strong>Микрозаём</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Класс качества активов:</span
              ><strong>Сомнительный</strong>
            </li>
          </ul>
          <ul class="list">
            <li class="item">
              <span class="num">9.</span><span>Валюта договора:</span
              ><strong>Узбекский сум (860)</strong>
            </li>

            <li class="item">
              <span class="num">10.</span><span>Процентная ставка: </span
              ><strong> 24</strong>
            </li>

            <li class="item">
              <span class="num">11.</span><span>Сумма договора: </span
              ><strong>5 000 000.00</strong>
            </li>

            <li class="item">
              <span class="num">12.</span><span>Выданная сумма: </span
              ><strong>5 000 000.00 </strong>
            </li>

            <li class="item">
              <span class="num">13.</span
              ><span>Закрытая судебная задолженность ОД:</span
              ><strong>1 000 000.00</strong>
            </li>

            <li class="item">
              <span class="num">14.</span
              ><span>Закрытая внебалансовая задолженность ОД:</span
              ><strong>0 </strong>
            </li>

            <li class="item">
              <span class="num">15.</span
              ><span>Закрытая внебалансовая задолженность %:</span
              ><strong>0 </strong>
            </li>
          </ul>
        </div> -->
        <div class="contents">
          <p>Просроченные платежи основного долга</p>
        </div>
        <div class="centre">
          <strong>Не имеется</strong>
        </div>
        <div class="chaild-title">
          <div class="">
            <strong class="tex-white">6.3 КРЕДИТОР:</strong
            ><span>ООО «MEGA» (301 000 890)</span>
          </div>
          <div class="">
            <strong class="tex-white">ТИП:</strong>
            <span>БАНК</span>
          </div>
        </div>
        <!-- <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Статус договора: </span
              ><strong>Закрыт (2018-03-23)</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Номер договора:</span
              ><strong> 4858</strong>
            </li>

            <li class="item">
              <span class="num">3.</span><span>. Дата начала договора:</span
              ><strong>: 2017-03-03</strong>
            </li>

            <li class="item">
              <span class="num">4.</span><span>Дата окончания договора: </span
              ><strong>2018-03-25</strong>
            </li>
          </ul>
          <ul class="list">
            <li class="item">
              <span class="num">5.</span><span>Номер и дата заявки: </span
              ><strong>398, 2017-03-03</strong>
            </li>

            <li class="item">
              <span class="num">6.</span><span>Вид кредита:</span
              ><strong>Рассрочка</strong>
            </li>

            <li class="item">
              <span class="num">7.</span><span>Валюта договора:</span
              ><strong>Доллар США (840)</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Сумма договора:</span
              ><strong>200.00</strong>
            </li>
          </ul>
        </div> -->
        <div class="contents">
          <p>Просроченные платежи основного долга</p>
        </div>
        <div class="centre">
          <strong>Не имеется</strong>
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title mt">
          <p class="info__title-text">7. УСЛОВНЫЕ ОБЯЗАТЕЛЬСТВА</p>
        </div>
        <div class="chaild-title">
          <div class="">
            <strong class="tex-white">7.1 КРЕДИТОР:</strong
            ><span
              >Тошкент ш., «Ипотека банк» АТИБ Олмазор филиали (00901)
            </span>
          </div>
          <div class="">
            <strong class="tex-white">ТИП:</strong>
            <span>БАНК</span>
          </div>
        </div>
        <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Статус договора: </span
              ><strong>{{
                infoScore.contingent_liabilities.contingent_liability
                  .contract_status
              }}</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Номер договора:</span
              ><strong>
                {{
                  infoScore.contingent_liabilities.contingent_liability
                    .contract_id
                }}</strong
              >
            </li>

            <li class="item">
              <span class="num">3.</span><span>Дата начала договора:</span
              ><strong>
                {{
                  infoScore.contingent_liabilities.contingent_liability
                    .contract_date
                }}</strong
              >
            </li>

            <li class="item">
              <span class="num">4.</span><span>Дата закрытия договора: </span
              ><strong>{{
                infoScore.contingent_liabilities.contingent_liability
                  .contract_end_date
              }}</strong>
            </li>

            <li class="item">
              <span class="num">5.</span><span>Валюта договора:</span
              ><strong>{{
                infoScore.contingent_liabilities.contingent_liability.currency
              }}</strong>
            </li>

            <li class="item">
              <span class="num">6.</span><span>Вид кредита:</span
              ><strong>{{ non }}</strong>
            </li>

            <li class="item">
              <span class="num">7.</span><span>Процентная ставка:</span
              ><strong>{{
                infoScore.contingent_liabilities.contingent_liability.percent
              }}</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Сумма договора:</span
              ><strong>{{ non }}</strong>
            </li>

            <li class="item">
              <span class="num">9.</span><span>Сумма обеспечения:</span
              ><strong>{{ non }}</strong>
            </li>
          </ul>
          <ul class="list">
            <li class="item">
              <span class="num">10.</span
              ><span>Остаток всей задолженности: </span
              ><strong
                >{{
                  infoScore.contingent_liabilities.contingent_liability
                    .total_debt_sum
                }}
              </strong>
            </li>

            <li class="item">
              <span class="num">11.</span
              ><span>Остаток просроченной задолженности:</span
              ><strong>{{
                infoScore.contingent_liabilities.contingent_liability
                  .overdue_debt_sum
              }}</strong>
            </li>

            <li class="item">
              <span class="num">12.</span
              ><span>Максимальная просрочка ОД (дни или статус):</span
              ><strong>{{ non }} </strong>
            </li>

            <li class="item">
              <span class="num">13.</span
              ><span
                >Максимальная непрерывная просрочка % (дни или статус):</span
              ><strong>{{ non }}</strong>
            </li>

            <li class="item">
              <span class="num">14.</span
              ><span>Максимальная текущая просрочка ОД (дни или статус): </span
              ><strong>{{ non }} </strong>
            </li>

            <li class="item">
              <span class="num">15.</span
              ><span
                >Максимальная текущая непрерывная просрочка % (дни или
                статус):</span
              ><strong>{{ non }} </strong>
            </li>
          </ul>
        </div>
        <div class="chaild-title">
          <div class="">
            <strong class="tex-white">7.2 КРЕДИТОР:</strong
            ><span
              >Тошкент ш., «Ипак йули» АИТБ Шайхонтохур филиали (01145)
            </span>
          </div>
          <div class="">
            <strong class="tex-white">ТИП:</strong>
            <span>БАНК</span>
          </div>
        </div>
        <!-- <div class="listse">
          <ul class="list">
            <li class="item">
              <span class="num">1.</span><span>Статус договора: </span
              ><strong>Закрыт</strong>
            </li>

            <li class="item">
              <span class="num">2.</span><span>Номер договора: </span
              ><strong> 5698</strong>
            </li>

            <li class="item">
              <span class="num">3.</span><span>Дата начала договора:</span
              ><strong>2009-08-07</strong>
            </li>

            <li class="item">
              <span class="num">4.</span><span>Дата закрытия договора: </span
              ><strong>2019-08-07</strong>
            </li>

            <li class="item">
              <span class="num">5.</span><span>Валюта договора: </span
              ><strong>Узбекский сум (860)</strong>
            </li>

            <li class="item">
              <span class="num">6.</span><span>Вид кредита:</span
              ><strong>Ипотека</strong>
            </li>
          </ul>
          <ul class="list">
            <li class="item">
              <span class="num">7.</span><span>Процентная ставка:</span
              ><strong>25</strong>
            </li>

            <li class="item">
              <span class="num">8.</span><span>Сумма договора:</span
              ><strong>160 000 000.00 </strong>
            </li>

            <li class="item">
              <span class="num">9.</span><span>Сумма обеспечения:</span
              ><strong>100 000 000.00</strong>
            </li>

            <li class="item">
              <span class="num">10.</span
              ><span>Максимальная просрочка ОД (дни или статус): </span
              ><strong>7</strong>
            </li>

            <li class="item">
              <span class="num">11.</span
              ><span
                >. Максимальная непрерывная просрочка % (дни или статус):</span
              ><strong>7</strong>
            </li>
          </ul>
        </div> -->
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title mt">
          <p class="info__title-text">
            8. ЗАПРОСЫ И ПОДПИСКИ ПО СУБЪЕКТУ КРЕДИТНОЙ ИНФОРМАЦИИ
          </p>
        </div>
        <div class="info__title pinks mt">
          <p class="info__title-text">8.1 ЗАПРОСЫ</p>
        </div>
        <div class="dogovor">
          <table class="table">
            <thead>
              <tr>
                <th class="">№</th>
                <th>ВРЕМЯ ЗАПРОСА</th>
                <th class="ww">ПОЛЬЗОВАТЕЛЬ</th>
                <th>КОД КО</th>
                <th>№ ЗАЯВКИ</th>
                <th>№ И ДАТА СОГЛАСИЯ</th>
              </tr>
            </thead>
            <tbody>
              <tr
                class="rosw"
                v-for="(item, index) in infoScore.credit_requests
                  .credit_request"
                :key="index"
              >
                <td class="number">{{ ++index }}</td>
                <td>{{ item.demand_date_time }}</td>
                <td class="ww">
                  {{ item.user_id }}
                </td>
                <td>{{ item.report_type }}</td>
                <td>{{ item.claim_id }}</td>
                <td>{{ item.consent_date }}</td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="info__title pinks mt">
          <p class="info__title-text">8.2 ПОДПИСКИ НА УВЕДОМЛЕНИЯ</p>
        </div>
        <div class="dogovor">
          <table class="table">
            <thead>
              <tr>
                <th class="">№</th>
                <th>ПЕРИОД ПОДПИСКИ</th>
                <th class="ww">ПОЛЬЗОВАТЕЛЬ</th>
                <th>№ ЗАЯВКИ</th>
                <th>№ И ДАТА СОГЛАСИЯ</th>
              </tr>
            </thead>
            <tbody>
              <tr
                class="rosw"
                v-for="(item, index) in infoScore.subscriptions.subscription"
                :key="index"
              >
                <td class="number">{{ ++index }}</td>
                <td>{{ item.subscription_period }}</td>
                <td class="ww">
                  {{ item.user_id }}
                </td>
                <td>{{ item.consent_id }}</td>
                <td>{{ item.consent_date }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </section>
    <section>
      <div class="container">
        <div class="info__title grin mt">
          <p class="info__title-text">9. ПРИМЕЧАНИЯ</p>
        </div>
        <ul class="lista">
          <li class="itms" v-for="(item, index) in text" :key="index">
            <span class="number">{{ ++index }}.</span>
            <p class="texts">
              {{ item.split("\t")[1] }}
            </p>
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { useI18n } from "vue-i18n";

let infoScore = {
  contingent_liabilities: {
    contingent_liability: [
      {
        amount: "",
        subject_type: "",
        overdue_debt_sum: "",
        org: "",
        contract_id: "",
        overdue_debt_sum_change: "",
        contract_status: "",
        branch: "",
        amount_change: "",
        percent: "",
        contract_end_date: "",
        max_current_overdue: "",
        contract_date: "",
        total_debt_sum: "",
        currency: "",
        total_debt_sum_change: "",
        percent_change: "",
      },
    ],
  },
  overview: {
    contingent_liabilities_qty: 0,
    max_overdue_principal_sum: 0,
    max_uninter_overdue_percent_days: 0,
    max_overdue_principal_days: 0,
    total_overdue_percent_sum: 0,
    credit_request_qty: 179,
    claims_qty: 49,
    average_monthly_payment: 175563302,
    subscriptions_qty: 0,
    contracts_qty: 4,
    overdue_principal_qty: 0,
  },
  subscriptions: {
    subscription: [
      {
        org: "",
        user_id: "",
        claim_id: "",
        subscription_period: "",
        consent_date: "",
        branch: "",
        consent_id: "",
      },
    ],
  },
  scorring: {
    scoring_version: "1.2",
    scoring_grade: "347",
    scoring_class: "B2",
    scoring_level: "ХОРОШИЙ",
  },
  sysinfo: {
    demand_id: "RET2022236743410",
    notes:
      "1.\tПредоставление и использование кредитной информации регулируется законом № ЗРУ-301 «Об обмене кредитной информацией» от 04.10.2011 г.\n2.\tКредитное бюро не проставляет запрета на кредитование, не вносит субъекта кредитной информации в «чёрный» список и не осуществляет никаких корректировок, исправлений, удалений в кредитную информацию, отражённой в кредитном отчёте. Внести изменения вправе, организация, предоставившая информацию, и только в случае, если данные переданы неверно или ошибочно.\n3.\tЕсли субъект кредитной информации не согласен с какой-либо информацией, содержащейся в кредитном отчёте, субъекту кредитной информации необходимо обратиться сперва к поставщику информации, а затем в кредитное бюро с заявлением об оспаривании информации.\n4.\tСкоринговый балл имеет рекомендательный характер и может быть основанием для выдачи или отказа кредитов только по усмотрению кредитора.\n5.\tНегативные факторы во время льготного периода в период пандемии с 01.03.2020-01.10.2020 не влияют на скоринговый балл.\n6.\tСреднемесячный платёж включает в себя расчёт исходя из остатков основного долга и прогнозного платежа по процентам (аннуитетный).\n7.\tКредиты в иностранной валюте в совокупных суммах рассчитывается в сумовом эквиваленте по курсу ЦБ РУз на дату формирования кредитного отчёта.\n8.\tПри изменениях расчётов меняется версия скорингового балла.",
    org: "RET",
    user_id: "TAQSIM SARMOYA (20176), System S.S",
    claim_id: "2c9b9105d5ed4855a03e",
    report_type: "077",
    consent_date: "2022- 08-24",
    report_name: "InfoScore (XML)",
    demand_date_time: "2022-08-24 12:51",
    branch: "20176",
    consent_id: "40",
    claim_date: "2022- 08-24",
  },
  credit_requests: {
    credit_request: [
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "2c9b9105d5ed4855a03e",
        report_type: "025",
        consent_date: "2022-08-24",
        demand_date_time: "2022-08-24 12:50",
        branch: "20176",
        consent_id: "40",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "2c9b9105d5ed4855a03e",
        report_type: "039",
        consent_date: "2022-08-24",
        demand_date_time: "2022-08-24 12:50",
        branch: "20176",
        consent_id: "40",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "2c9b9105d5ed4855a03e",
        report_type: "077",
        consent_date: "2022-08-24",
        demand_date_time: "2022-08-24 12:51",
        branch: "20176",
        consent_id: "40",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "6cfa7f62e85741b282d7",
        report_type: "025",
        consent_date: "2022-08-18",
        demand_date_time: "2022-08-18 11:50",
        branch: "20176",
        consent_id: "41",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "6cfa7f62e85741b282d7",
        report_type: "039",
        consent_date: "2022-08-18",
        demand_date_time: "2022-08-18 11:49",
        branch: "20176",
        consent_id: "41",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "6cfa7f62e85741b282d7",
        report_type: "077",
        consent_date: "2022-08-18",
        demand_date_time: "2022-08-18 11:50",
        branch: "20176",
        consent_id: "41",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "f59f399527ef491784b8",
        report_type: "025",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 18:09",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "f59f399527ef491784b8",
        report_type: "039",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 18:09",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "f59f399527ef491784b8",
        report_type: "070",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 18:09",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "f59f399527ef491784b8",
        report_type: "077",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 18:10",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "d1fee367b6ba4c318080",
        report_type: "025",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 16:34",
        branch: "20176",
        consent_id: "39",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "d1fee367b6ba4c318080",
        report_type: "039",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 16:34",
        branch: "20176",
        consent_id: "39",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "d1fee367b6ba4c318080",
        report_type: "070",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 16:34",
        branch: "20176",
        consent_id: "39",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "d1fee367b6ba4c318080",
        report_type: "077",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 16:35",
        branch: "20176",
        consent_id: "39",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "689cf21a3d284e70a095",
        report_type: "025",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 14:42",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "689cf21a3d284e70a095",
        report_type: "039",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 14:41",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "689cf21a3d284e70a095",
        report_type: "070",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 14:42",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "689cf21a3d284e70a095",
        report_type: "077",
        consent_date: "2022-07-29",
        demand_date_time: "2022-07-29 14:42",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "7ca36cf6508c4056a84e",
        report_type: "025",
        consent_date: "2022-07-19",
        demand_date_time: "2022-07-19 16:00",
        branch: "20176",
        consent_id: "14",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "7ca36cf6508c4056a84e",
        report_type: "039",
        consent_date: "2022-07-19",
        demand_date_time: "2022-07-19 15:59",
        branch: "20176",
        consent_id: "14",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "7ca36cf6508c4056a84e",
        report_type: "070",
        consent_date: "2022-07-19",
        demand_date_time: "2022-07-19 16:00",
        branch: "20176",
        consent_id: "14",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "7ca36cf6508c4056a84e",
        report_type: "077",
        consent_date: "2022-07-19",
        demand_date_time: "2022-07-19 16:00",
        branch: "20176",
        consent_id: "14",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ccf06e79301845f3954f",
        report_type: "025",
        consent_date: "2022-07-07",
        demand_date_time: "2022-07-07 17:28",
        branch: "20176",
        consent_id: "31",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ccf06e79301845f3954f",
        report_type: "039",
        consent_date: "2022-07-07",
        demand_date_time: "2022-07-07 17:27",
        branch: "20176",
        consent_id: "31",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ccf06e79301845f3954f",
        report_type: "070",
        consent_date: "2022-07-07",
        demand_date_time: "2022-07-07 17:28",
        branch: "20176",
        consent_id: "31",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ccf06e79301845f3954f",
        report_type: "077",
        consent_date: "2022-07-07",
        demand_date_time: "2022-07-07 17:28",
        branch: "20176",
        consent_id: "31",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "34a21866a9994e5d9989",
        report_type: "025",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 17:27",
        branch: "20176",
        consent_id: "13",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "34a21866a9994e5d9989",
        report_type: "039",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 17:27",
        branch: "20176",
        consent_id: "13",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "34a21866a9994e5d9989",
        report_type: "070",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 17:27",
        branch: "20176",
        consent_id: "13",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "34a21866a9994e5d9989",
        report_type: "077",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 17:28",
        branch: "20176",
        consent_id: "13",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "a1a05eaaeaa74a34be75",
        report_type: "025",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 12:03",
        branch: "20176",
        consent_id: "12",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "a1a05eaaeaa74a34be75",
        report_type: "039",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 12:03",
        branch: "20176",
        consent_id: "12",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "a1a05eaaeaa74a34be75",
        report_type: "070",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 12:03",
        branch: "20176",
        consent_id: "12",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "a1a05eaaeaa74a34be75",
        report_type: "077",
        consent_date: "2022-07-01",
        demand_date_time: "2022-07-01 12:03",
        branch: "20176",
        consent_id: "12",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00378810",
        report_type: "008",
        consent_date: "2022-06-30",
        demand_date_time: "2022-07-01 16:58",
        branch: "01145",
        consent_id: "F00378810",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "21094289048e4170a35f",
        report_type: "025",
        consent_date: "2022-06-25",
        demand_date_time: "2022-06-25 14:36",
        branch: "20176",
        consent_id: "8",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "21094289048e4170a35f",
        report_type: "039",
        consent_date: "2022-06-25",
        demand_date_time: "2022-06-25 14:35",
        branch: "20176",
        consent_id: "8",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "21094289048e4170a35f",
        report_type: "070",
        consent_date: "2022-06-25",
        demand_date_time: "2022-06-25 14:36",
        branch: "20176",
        consent_id: "8",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "21094289048e4170a35f",
        report_type: "077",
        consent_date: "2022-06-25",
        demand_date_time: "2022-06-25 14:37",
        branch: "20176",
        consent_id: "8",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "8e3aa3969ab24971be2a",
        report_type: "025",
        consent_date: "2022-06-22",
        demand_date_time: "2022-06-22 19:59",
        branch: "20176",
        consent_id: "27",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "8e3aa3969ab24971be2a",
        report_type: "039",
        consent_date: "2022-06-22",
        demand_date_time: "2022-06-22 19:59",
        branch: "20176",
        consent_id: "27",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "8e3aa3969ab24971be2a",
        report_type: "070",
        consent_date: "2022-06-22",
        demand_date_time: "2022-06-22 19:59",
        branch: "20176",
        consent_id: "27",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "8e3aa3969ab24971be2a",
        report_type: "077",
        consent_date: "2022-06-22",
        demand_date_time: "2022-06-22 19:59",
        branch: "20176",
        consent_id: "27",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "129b7e3a70484fae84fa",
        report_type: "025",
        consent_date: "2022-06-12",
        demand_date_time: "2022-06-12 13:40",
        branch: "20176",
        consent_id: "4",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "129b7e3a70484fae84fa",
        report_type: "039",
        consent_date: "2022-06-12",
        demand_date_time: "2022-06-12 13:40",
        branch: "20176",
        consent_id: "4",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "129b7e3a70484fae84fa",
        report_type: "070",
        consent_date: "2022-06-12",
        demand_date_time: "2022-06-12 13:40",
        branch: "20176",
        consent_id: "4",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "129b7e3a70484fae84fa",
        report_type: "077",
        consent_date: "2022-06-12",
        demand_date_time: "2022-06-12 13:41",
        branch: "20176",
        consent_id: "4",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "226cc4877eb6462dbeb0",
        report_type: "025",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 19:01",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "226cc4877eb6462dbeb0",
        report_type: "039",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 19:00",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "226cc4877eb6462dbeb0",
        report_type: "070",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 19:01",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "226cc4877eb6462dbeb0",
        report_type: "077",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 19:01",
        branch: "20176",
        consent_id: "23",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "732ea2d24ab6428ab24c",
        report_type: "025",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 10:59",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "732ea2d24ab6428ab24c",
        report_type: "039",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 10:58",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "732ea2d24ab6428ab24c",
        report_type: "070",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 10:59",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "732ea2d24ab6428ab24c",
        report_type: "077",
        consent_date: "2022-06-10",
        demand_date_time: "2022-06-10 11:00",
        branch: "20176",
        consent_id: "19",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1014",
        report_type: "025",
        consent_date: "2022-05-14",
        demand_date_time: "2022-05-14 09:37",
        branch: "20176",
        consent_id: "418",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1014",
        report_type: "039",
        consent_date: "2022-05-14",
        demand_date_time: "2022-05-14 09:37",
        branch: "20176",
        consent_id: "418",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1014",
        report_type: "070",
        consent_date: "2022-05-14",
        demand_date_time: "2022-05-14 09:37",
        branch: "20176",
        consent_id: "418",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1014",
        report_type: "077",
        consent_date: "2022-05-14",
        demand_date_time: "2022-05-14 09:37",
        branch: "20176",
        consent_id: "418",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "025",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 11:34",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "025",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 17:23",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "025",
        consent_date: "2022-05-06",
        demand_date_time: "2022-06-01 14:56",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "039",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 11:34",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "039",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 17:23",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "070",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 11:34",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "070",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 17:23",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "1003",
        report_type: "077",
        consent_date: "2022-05-06",
        demand_date_time: "2022-05-06 17:24",
        branch: "20176",
        consent_id: "408",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "025",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 16:01",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "025",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-22 10:42",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "039",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 16:01",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "039",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-22 10:42",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "070",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 16:01",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "070",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-22 10:42",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "077",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 16:02",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "364",
        report_type: "077",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-22 10:42",
        branch: "20176",
        consent_id: "389",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "359",
        report_type: "025",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:19",
        branch: "20176",
        consent_id: "388",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "359",
        report_type: "039",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:18",
        branch: "20176",
        consent_id: "388",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "359",
        report_type: "070",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:18",
        branch: "20176",
        consent_id: "388",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "359",
        report_type: "077",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:19",
        branch: "20176",
        consent_id: "388",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "025",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 11:27",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "025",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:02",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "039",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 11:27",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "039",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:02",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "070",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 11:27",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "070",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:02",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "077",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 11:27",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "358",
        report_type: "077",
        consent_date: "2022-04-21",
        demand_date_time: "2022-04-21 12:02",
        branch: "20176",
        consent_id: "384",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "348",
        report_type: "025",
        consent_date: "2022-04-19",
        demand_date_time: "2022-04-19 15:35",
        branch: "20176",
        consent_id: "380",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "348",
        report_type: "039",
        consent_date: "2022-04-19",
        demand_date_time: "2022-04-19 15:35",
        branch: "20176",
        consent_id: "380",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "348",
        report_type: "070",
        consent_date: "2022-04-19",
        demand_date_time: "2022-04-19 15:35",
        branch: "20176",
        consent_id: "380",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "348",
        report_type: "077",
        consent_date: "2022-04-19",
        demand_date_time: "2022-04-19 15:35",
        branch: "20176",
        consent_id: "380",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "025",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 11:05",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "025",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 22:41",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "039",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 11:05",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "039",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 22:41",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "070",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 11:05",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "070",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 22:41",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "077",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 11:05",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "317",
        report_type: "077",
        consent_date: "2022-04-14",
        demand_date_time: "2022-04-14 22:41",
        branch: "20176",
        consent_id: "341",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "300",
        report_type: "023",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-11 09:34",
        branch: "20176",
        consent_id: "331",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "300",
        report_type: "025",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:47",
        branch: "20176",
        consent_id: "331",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "300",
        report_type: "039",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:47",
        branch: "20176",
        consent_id: "331",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "300",
        report_type: "070",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:47",
        branch: "20176",
        consent_id: "331",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "300",
        report_type: "077",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:48",
        branch: "20176",
        consent_id: "331",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "298",
        report_type: "025",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:17",
        branch: "20176",
        consent_id: "330",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "298",
        report_type: "039",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:17",
        branch: "20176",
        consent_id: "330",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "298",
        report_type: "070",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:17",
        branch: "20176",
        consent_id: "330",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "298",
        report_type: "077",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 10:17",
        branch: "20176",
        consent_id: "330",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00303589",
        report_type: "008",
        consent_date: "2022-04-07",
        demand_date_time: "2022-04-07 21:16",
        branch: "01145",
        consent_id: "F00303589",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "025",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 16:16",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "025",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 17:00",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "039",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 16:16",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "039",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 17:00",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "070",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 16:16",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "070",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 17:00",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "077",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 16:17",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "295",
        report_type: "077",
        consent_date: "2022-04-06",
        demand_date_time: "2022-04-06 17:00",
        branch: "20176",
        consent_id: "328",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "292",
        report_type: "025",
        consent_date: "2022-04-05",
        demand_date_time: "2022-04-05 12:38",
        branch: "20176",
        consent_id: "324",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "292",
        report_type: "039",
        consent_date: "2022-04-05",
        demand_date_time: "2022-04-05 12:38",
        branch: "20176",
        consent_id: "324",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "292",
        report_type: "070",
        consent_date: "2022-04-05",
        demand_date_time: "2022-04-05 12:38",
        branch: "20176",
        consent_id: "324",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "292",
        report_type: "077",
        consent_date: "2022-04-05",
        demand_date_time: "2022-04-05 12:39",
        branch: "20176",
        consent_id: "324",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "025",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 17:18",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "025",
        consent_date: "2022-03-30",
        demand_date_time: "2022-04-04 11:57",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "039",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 17:18",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "039",
        consent_date: "2022-03-30",
        demand_date_time: "2022-04-04 11:57",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "070",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 17:18",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "070",
        consent_date: "2022-03-30",
        demand_date_time: "2022-04-04 11:57",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "077",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 17:19",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "285",
        report_type: "077",
        consent_date: "2022-03-30",
        demand_date_time: "2022-04-04 11:57",
        branch: "20176",
        consent_id: "312",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "025",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 14:56",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "025",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 16:29",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "039",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 14:55",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "039",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 16:29",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "070",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 14:55",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "070",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 16:29",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "077",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 14:56",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "210",
        report_type: "077",
        consent_date: "2022-03-30",
        demand_date_time: "2022-03-30 16:29",
        branch: "20176",
        consent_id: "309",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "025",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-17 14:08",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "025",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 16:07",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "025",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 17:21",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "025",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 18:36",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "025",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 20:29",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "039",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-17 14:07",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "039",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 16:07",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "039",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 17:20",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "039",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 18:36",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "039",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 20:29",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "070",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-17 14:08",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "070",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 16:07",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "070",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 17:20",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "070",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 18:36",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "070",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 20:29",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "077",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-17 14:08",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "077",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 16:07",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "077",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 17:21",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "077",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 18:37",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "124",
        report_type: "077",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-18 20:29",
        branch: "20176",
        consent_id: "0",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00265430",
        report_type: "008",
        consent_date: "2022-02-17",
        demand_date_time: "2022-02-17 21:31",
        branch: "01145",
        consent_id: "F00265430",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00265430",
        report_type: "008",
        consent_date: "2022-02-17",
        demand_date_time: "2022-03-11 15:43",
        branch: "01145",
        consent_id: "F00265430",
      },
      {
        org: "014",
        user_id: "(система)",
        claim_id: "36533",
        report_type: "001",
        consent_date: "2022-01-17",
        demand_date_time: "2022-03-09 18:35",
        branch: "01145",
        consent_id: "36533",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00241967",
        report_type: "008",
        consent_date: "2022-01-16",
        demand_date_time: "2022-01-16 20:47",
        branch: "01145",
        consent_id: "F00241967",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "36811",
        report_type: "008",
        consent_date: "2021-11-01",
        demand_date_time: "2021-11-01 18:00",
        branch: "20002",
        consent_id: "0000036811",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "36811",
        report_type: "039",
        consent_date: "2021-11-01",
        demand_date_time: "2021-11-01 18:01",
        branch: "20002",
        consent_id: "0000036811",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00192603",
        report_type: "008",
        consent_date: "2021-11-01",
        demand_date_time: "2021-11-01 17:19",
        branch: "00444",
        consent_id: "F00192603",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00192603",
        report_type: "008",
        consent_date: "2021-11-01",
        demand_date_time: "2021-11-01 18:05",
        branch: "00444",
        consent_id: "F00192603",
      },
      {
        org: "014",
        user_id: "System S.S.",
        claim_id: "F00192603",
        report_type: "008",
        consent_date: "2021-11-01",
        demand_date_time: "2021-11-02 00:01",
        branch: "00444",
        consent_id: "F00192603",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "2f5b728472",
        report_type: "023",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:34",
        branch: "20100",
        consent_id: "2f5b728472",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "177abd312a",
        report_type: "023",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:34",
        branch: "20100",
        consent_id: "177abd312a",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "007",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "022",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "022",
        consent_date: "2021-10-29",
        demand_date_time: "2021-11-01 17:30",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "023",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "025",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "039",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "039",
        consent_date: "2021-10-29",
        demand_date_time: "2021-11-01 17:30",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "155",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "RET",
        user_id: "System S.S.",
        claim_id: "ac346309a398277",
        report_type: "177",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:13",
        branch: "20038",
        consent_id: "398277",
      },
      {
        org: "009",
        user_id: "System S.S.",
        claim_id: "796929",
        report_type: "022",
        consent_date: "2021-10-29",
        demand_date_time: "2021-10-29 15:01",
        branch: "01037",
        consent_id: "1",
      },
      {
        org: "048",
        user_id: "(система)",
        claim_id: "202664",
        report_type: "003",
        consent_date: "2020-01-22",
        demand_date_time: "2020-01-22 11:29",
        branch: "00996",
        consent_id: "5554",
      },
    ],
  },
  client: {
    pinfl: "33103940270022",
    live_address: "",
    registration_region: "0",
    gender: "M",
    registration_district: "0",
    birth_date: "1994-03-31",
    inn: "",
    client_type: "08",
    founders: "",
    oked: "",
    email_change: "2022-08-24",
    juridical_status: "2",
    name: "SULTANBAYEV SHERZOD SARVAR O‘G‘LI",
    live_address_change: "2022-08-24",
    registration_address: "adres",
    email: "н/д",
    registration_address_change: "2022-08-24",
  },
  blacklist: null,
  open_contracts: {
    open_contract: [
      {
        monthly_average_payment: "137685641",
        overdue_debt_sum: "0",
        org: "014",
        contract_id: "MZ_ONLINE 319010",
        total_debt_sum: "1205950301",
        currency: "000",
        branch: "01145",
      },
      {
        monthly_average_payment: "37877661",
        overdue_debt_sum: "0",
        org: "048",
        contract_id: "297606",
        total_debt_sum: "568164913",
        currency: "000",
        branch: "01186",
      },
    ],
  },
  claims_wo_contracts: {
    claim_wo_contract: [
      {
        rejection_date: "2021-12-02",
        summa: "",
        org: "014",
        claim_id: "F00192603",
        rejection_reason: "08",
        currency: "н\\д",
        branch: "00444",
        claim_date: "2021-11-01",
      },
      {
        rejection_date: "2022-02-16",
        summa: "",
        org: "014",
        claim_id: "F00241967",
        rejection_reason: "08",
        currency: "н\\д",
        branch: "01145",
        claim_date: "2022-01-16",
      },
      {
        rejection_date: "2022-03-20",
        summa: "",
        org: "014",
        claim_id: "F00265430",
        rejection_reason: "08",
        currency: "н\\д",
        branch: "01145",
        claim_date: "2022-02-17",
      },
      {
        rejection_date: "2022-05-09",
        summa: "",
        org: "014",
        claim_id: "F00303589",
        rejection_reason: "08",
        currency: "н\\д",
        branch: "01145",
        claim_date: "2022-04-07",
      },
      {
        rejection_date: "2022-07-31",
        summa: "",
        org: "014",
        claim_id: "F00378810",
        rejection_reason: "08",
        currency: "н\\д",
        branch: "01145",
        claim_date: "2022-06-30",
      },
      {
        rejection_date: "2021-11-01",
        summa: "",
        org: "RET",
        claim_id: "36811",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20002",
        claim_date: "2021-11-01",
      },
      {
        rejection_date: "2021-11-30",
        summa: "",
        org: "RET",
        claim_id: "ac346309a398277",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20038",
        claim_date: "2021-10-29",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "177abd312a",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20100",
        claim_date: "2021-10-29",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "2f5b728472",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20100",
        claim_date: "2021-10-29",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "1003",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-05-06",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "10098240722",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2021-11-19",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "10098240723",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2021-11-19",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "10098240730",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2021-11-19",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "1014",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-05-14",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "124",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-02-17",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "129b7e3a70484fae84fa",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-06-12",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "141d2d2cfd164511aaff",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-26",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "210",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-03-30",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "21094289048e4170a35f",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-06-25",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "226cc4877eb6462dbeb0",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-06-10",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "285",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-03-30",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "292",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-05",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "295",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-06",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "298",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-07",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "2c9b9105d5ed4855a03e",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-08-24",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "300",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-07",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "317",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-14",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "348",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-19",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "34a21866a9994e5d9989",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-01",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "358",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-21",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "359",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-21",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "364",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-04-21",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "4ec2c18e4f7b413a84f5",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-29",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "689cf21a3d284e70a095",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-29",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "6cfa7f62e85741b282d7",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-08-18",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "732ea2d24ab6428ab24c",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-06-10",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "7ca36cf6508c4056a84e",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-19",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "88",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-02-05",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "8e3aa3969ab24971be2a",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-06-22",
      },
      {
        rejection_date: "2022-07-01",
        summa: "",
        org: "RET",
        claim_id: "a1a05eaaeaa74a34be75",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-01",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "ccf06e79301845f3954f",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-07",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "d1fee367b6ba4c318080",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-29",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "f59f399527ef491784b8",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20176",
        claim_date: "2022-07-29",
      },
      {
        rejection_date: "",
        summa: "",
        org: "RET",
        claim_id: "10098240740",
        rejection_reason: "",
        currency: "н\\д",
        branch: "20177",
        claim_date: "2021-11-19",
      },
    ],
  },
  contracts: {
    contract: [
      {
        contract_id: "38262",
        security_qty: "0",
        contract_status: "1",
        claim_id: "38262",
        branch: "01145",
        claim_id_change: "2022-07-01",
        percent: "34.9",
        amount_change: "2022-07-01",
        immediate_principal_sum_change: "2022-07-29",
        securities: null,
        contract_end_date: "2023-06-30",
        contract_date: "2022-07-01",
        class_asset_quality: "1",
        total_debt_sum: "1205950301",
        contract_end_date_change: "2022-07-01",
        remaining_limit_sum: "0",
        currency: "000",
        immediate_principal_sum: "1180000000",
        ID: "1",
        percent_change: "2022-07-01",
        amount_issued_change: "2022-07-29",
        amount: "1350000000",
        contract_date_change: "2022-07-01",
        org: "014",
        org_type: "БАНК",
        amount_issued: "1350000000",
        credit_type: "36",
        juridical_status: "08",
        total_debt_sum_change: "2022-07-29",
        claim_date: "2022-07-01",
        class_asset_quality_change: "2022-07-01",
        lawsuit_principal_sum: "",
        offbalance_princial_sum: "",
        actual_schedule: {
          actual_schedule_change: "2022-07-29",
          actual_repayment: [
            {
              principal_sum: "170000000",
              repayment_date: "2022-07-29",
              remaining_principal_sum: "1180000000",
              percent_sum: "",
            },
          ],
        },
        forecasted_schedule: null,
        overdue_principals: null,
      },
      {
        contract_id: "297606",
        security_qty: "0",
        contract_status: "1",
        claim_id: "317049",
        branch: "01186",
        claim_id_change: "2021-07-19",
        percent: "0",
        amount_change: "2021-07-23",
        immediate_principal_sum_change: "2022-07-29",
        securities: null,
        contract_end_date: "2023-11-22",
        contract_date: "2020-01-23",
        class_asset_quality: "1",
        total_debt_sum: "568164913",
        contract_end_date_change: "2021-07-23",
        remaining_limit_sum: "0",
        currency: "000",
        immediate_principal_sum: "568164913",
        ID: "2",
        percent_change: "2021-07-23",
        amount_issued_change: "2022-07-29",
        amount: "1800000000",
        contract_date_change: "2021-07-23",
        org: "048",
        org_type: "БАНК",
        amount_issued: "1634868626",
        credit_type: "58",
        juridical_status: "08",
        total_debt_sum_change: "2022-07-29",
        claim_date: "2020-01-22",
        class_asset_quality_change: "2021-07-23",
        lawsuit_principal_sum: "",
        offbalance_princial_sum: "",
        actual_schedule: null,
        forecasted_schedule: {
          forecasted_schedule_change: "2021-07-23",
          forecasted_schedule_change_qty: 1,
          forecasted_payment: [
            {
              forecasted_payment_period: "2022-05",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-06",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-07",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-08",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-09",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-10",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-11",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2022-12",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-01",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-02",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-03",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-04",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-05",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-06",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-07",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-08",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-09",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-10",
              principal_sum: "94736800",
              percent_sum: "0",
            },
            {
              forecasted_payment_period: "2023-11",
              principal_sum: "94737600",
              percent_sum: "0",
            },
          ],
        },
        overdue_principals: null,
      },
      {
        contract_id: "36533",
        security_qty: "0",
        contract_status: "2",
        claim_id: "36533",
        branch: "01145",
        claim_id_change: "2022-01-18",
        percent: "34.9",
        amount_change: "2022-01-18",
        immediate_principal_sum_change: null,
        securities: null,
        contract_end_date: "2023-01-16",
        contract_date: "2022-01-17",
        class_asset_quality: "1",
        total_debt_sum: null,
        contract_end_date_change: "2022-01-18",
        remaining_limit_sum: null,
        currency: "000",
        immediate_principal_sum: null,
        ID: "3",
        percent_change: "2022-01-18",
        amount_issued_change: "04-JUL-22",
        amount: "1350000000",
        contract_date_change: "2022-01-18",
        org: "014",
        org_type: "БАНК",
        amount_issued: "1350000000",
        credit_type: "36",
        juridical_status: "08",
        total_debt_sum_change: null,
        claim_date: "2022-01-17",
        class_asset_quality_change: "2022-01-18",
        lawsuit_principal_sum: null,
        offbalance_princial_sum: null,
        actual_schedule: null,
        forecasted_schedule: null,
        overdue_principals: null,
      },
      {
        contract_id: "193955",
        security_qty: "0",
        contract_status: "2",
        claim_id: "202664",
        branch: "00996",
        claim_id_change: "2020-01-22",
        percent: "0",
        amount_change: "2020-01-23",
        immediate_principal_sum_change: null,
        securities: null,
        contract_end_date: "2023-11-22",
        contract_date: "2020-01-23",
        class_asset_quality: "1",
        total_debt_sum: null,
        contract_end_date_change: "2020-01-23",
        remaining_limit_sum: null,
        currency: "000",
        immediate_principal_sum: null,
        ID: "4",
        percent_change: "2020-01-23",
        amount_issued_change: "17-JUL-21",
        amount: "1800000000",
        contract_date_change: "2020-01-23",
        org: "048",
        org_type: "БАНК",
        amount_issued: "2360060237",
        credit_type: "58",
        juridical_status: "08",
        total_debt_sum_change: null,
        claim_date: "2020-01-22",
        class_asset_quality_change: "2020-01-23",
        lawsuit_principal_sum: null,
        offbalance_princial_sum: null,
        actual_schedule: null,
        forecasted_schedule: null,
        overdue_principals: null,
      },
    ],
  },
};
let text = ref(infoScore.sysinfo.notes.split("\n"));

let scoring = ref(infoScore.scorring.scoring_class[0]);
let scoringTitle = ref("");
if (scoring.value == "E") {
  scoringTitle = "ПЛОХОЙ";
}
if (scoring.value == "D") {
  scoringTitle = "СЛАБЫЙ";
}
if (scoring.value == "C") {
  scoringTitle = "СРЕДНИЙ";
}
if (scoring.value == "B") {
  scoringTitle = "ХОРОШИЙ";
}
if (scoring.value == "A") {
  scoringTitle = "ОТЛИЧНЫЙ";
}
</script>
<style lang="scss" scoped></style>
