# metadata-cts.json — CTS identity sidecar

Canonical CTS work URN + linked resources (PHI id, Wikidata work/author QIDs) per
Tesserae fileid. Loaded by latincy-readers as a secondary metadata file (fill-only;
public `metadata.json` values take precedence). Purpose: let downstream consumers
(e.g. the Lewis & Short WSD inversion) resolve `citation → work → file` by lookup
instead of surface-matching.

## Coverage (honest, partial)

- **Files with a CTS URN: 593 / 826**
- **Works (workkeys) resolved: 157 / 261**
- Of resolved works, 468 files carry Wikidata work QIDs; all carry PHI ids where
  the work is in PHI (`phi_id` is the P8311 literal, so a QID is derivable downstream).
- 93 files use `cts_urns` (a list) + `multi_work: true`: their Tesserae workkey
  aggregates several CTS works (biblical books under `jerome.vulgate`, collected Lives in
  `nepos.vitae`). Per-part URN resolution — matching each file/part to its specific book —
  is left as a TODO rather than assigning one (wrong) URN.

## Provenance

Every URN here is **validated**, not guessed:
- `cts_source: empirical-surface-bind` — from `tesserae-collection.json`, where the L&S
  quote surfaces for the work were found in this Tesserae text (Perseus P8311/P6941 QIDs).
- `cts_source: session-rebind-validated` — recovered 2026-08-04 by full-scale surface
  rebind (`latincy-wsd/scratch/coverage_iterate.py`); same standard.

No CTS URN was fabricated. The resolved set is the L&S-cited classical core (Cicero, Livy,
Vergil, Ovid, Horace, Caesar, Seneca, Tacitus, Plautus, …).

## Not yet resolved (104 workkeys)

Mostly late-antique / patristic / imperial authors Lewis & Short does not cite, so this
session's L&S-driven binding did not reach them. Fill from an authoritative CTS catalog
(PerseusDL `canonical-latinLit` textgroup/work URNs) or per-work Wikidata P8311:

- ammianus.rerum_gestarum
- anonymous.laudes_domini
- apuleius.apologia
- apuleius.florida
- apuleius.metamorphoses
- aristotle.economics_book_3
- augustine.de_doctrina_christiana
- augustine.epistulae_selections
- aurelius_victor.de_caesaribus
- aurelius_victor.epitome_de_caesaribus
- ausonius.cento_nuptialis
- ausonius.commemoratio_professorum_burdigalensium
- ausonius.cupido_cruciatus
- ausonius.de_bissula
- ausonius.de_herediolo
- ausonius.de_xii_caesaribus
- ausonius.eclogarum_liber
- ausonius.ephemeris_id_est_totius_diei_negotium
- ausonius.epicedion_in_patrem
- ausonius.epigrammata_ausonii_de_diversis_rebus
- ausonius.epistularum
- ausonius.epitaphia_heroum_qui_bello_troico_interfuerunt
- ausonius.gratiarum_actio
- ausonius.griphus_ternarii_numeri
- ausonius.libri_de_fastis_conclusio
- ausonius.ludus_septem_sapientum
- ausonius.mosella
- ausonius.oratio_consulis_ausonii_versibus_rhopalicis
- ausonius.ordo_urbium_nobilium
- ausonius.parentalia
- ausonius.praefatiunculae
- ausonius.precationes
- ausonius.technopaegnion
- ausonius.versus_paschales_pro_augusto_dicti
- bede.historiam_ecclesiasticam_gentis_anglorum
- boethius.consolatio_philosophiae
- boethius.de_fide_catholica
- boethius.liber_de_persona_et_duabus_naturis_contra_eutychen_et_nestorium
- boethius.quomodo_substantiae_in_eo_quod_sint_bonae_sint_cum_non_sint_substantialia_bona
- boethius.quomodo_trinitas
- boethius.utrum_pater
- caesar_augustus.res_gestae_divi_augusti
- cicero.academica
- cicero.letters_to_brutus
- cicero.lucullus
- cicero.pro_l_flacco
- claudian.carmina_minora
- claudian.de_bello_gildonico
- claudian.de_bello_gothico
- claudian.de_consulatu_stilichonis
- claudian.de_raptu_proserpinae
- claudian.epithalamium_de_nuptiis_honorii_augusti
- claudian.in_consulatum_olybrii_et_probini
- claudian.in_eutropium
- claudian.in_rufinum
- claudian.panegyricus_de_quarto_consulatu_honorii_augusti
- claudian.panegyricus_de_sexto_consulatu_honorii_augusti
- claudian.panegyricus_de_tertio_consulatu_honorii_augusti
- claudian.panegyricus_dictus_manlio_theodoro_consuli
- corippus.johannis
- dracontius.de_laudibus_dei
- dracontius.orestes
- dracontius.romulea
- dracontius.satisfactio
- ennius.annales
- ennodius.opera
- eutropius.brevarium
- glass.washingtonii_vita
- horace.ars_poetica
- horace.carmen_saeculare
- horace.epistles
- italicus.ilias_latina
- jerome.epistulae
- juvencus.historia_evangelica
- macrobius.fragment
- macrobius.saturnalia
- manilius.astronomicon
- marcus_mincuius_felix.octavius
- ovid.remedia_amoris
- paulus_diaconus.carmina
- petronius.satyricon
- pliny_the_younger.letters
- polignac.antilucretius
- polignac.epia
- polignac.imitatio
- priscian.carmen_in_laudem_Anastasii_imperatoris
- priscian.perihegesis
- prudentius.apotheosis
- prudentius.contra_symmachum
- prudentius.dittochaeon
- prudentius.epilogus
- prudentius.hamartigenia
- prudentius.psychomachia
- pseudo_cicero.in_sallustium
- pseudo_quintilian.major_declamations
- rutilius.de_reditu
- scriptores_historiae_augustae.historia_augusta
- seneca.octavia
- seneca_the_elder.excerpta_controversiae
- seneca_the_elder.fragmenta
- servius_honoratus.in_virgilii_georgicon_libros_commentarius
- silius_italicus.punica
- tertullian.apologeticum
- tertullian.de_spectaculis
