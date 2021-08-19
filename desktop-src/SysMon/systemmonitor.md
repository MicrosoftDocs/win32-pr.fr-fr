---
title: Objet SystemMonitor (Isysmon. h)
description: Cette classe contient les méthodes et les propriétés utilisées pour configurer le contrôle du moniteur système.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- SystemMonitor, objet SysMon
- Description de l’objet SystemMonitor SysMon
topic_type:
- apiref
api_name:
- SystemMonitor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b9489c2e966abdf3c329d952a76bd30de487cca99a3e00c8ff46431a163ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954504"
---
# <a name="systemmonitor-object"></a>Objet SystemMonitor

Cette classe contient les méthodes et les propriétés utilisées pour configurer le contrôle du moniteur système.

## <a name="members"></a>Membres

L’objet **systemmonitor** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

L’objet **systemmonitor** contient ces événements.



| Événement                                                         | Description                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounterAdded**](systemmonitor-oncounteradded.md)        | Vous avertit lorsqu’un compteur est ajouté à la collection de [**compteurs**](counters.md) .<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | Vous avertit avant qu’un compteur soit supprimé de la collection de [**compteurs**](counters.md) .<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | Vous avertit lorsqu’un compteur est sélectionné.<br/>                                                                         |
| [**OnDblClick**](-systemmonitor-ondblclick.md)               | Vous avertit quand un utilisateur double-clique sur la ligne de graphique, sur la barre d’histogramme ou sur l’élément de rapport avec le bouton gauche de la souris.<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | Vous avertit lorsque des exemples de valeurs pour les compteurs ont été collectés.<br/>                                            |



 

### <a name="methods"></a>Méthodes

L’objet **systemmonitor** a ces méthodes.



| Méthode                                                       | Description                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchLocking**](systemmonitor-batchinglock.md)           | Verrouille le moniteur système pour l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal.<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | Affiche la boîte de dialogue **Ajouter un compteur** .<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Efface tous les champs de données dans le contrôle.<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | Échantillonne une valeur pour chaque compteur dans l’objet de collection de **compteurs** .<br/>                                                                                       |
| [**Copier**](systemmonitor-copy.md)                           | Copie les paramètres de propriété, la liste de compteurs et les données de compteur du contrôle dans le presse-papiers sous la forme d’un objet HTML.<br/>                                                |
| [**DisplayProperties**](systemmonitor-displayproperties.md) | affiche la boîte de dialogue **propriétés du Graph** .<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | Récupère la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Ajoute les compteurs dans le fichier de modèle HTML au moniteur système.<br/>                                                                                            |
| [**Insérer**](systemmonitor-paste.md)                         | Ajoute la liste des compteurs copiés dans le presse-papiers à la collection actuelle de compteurs. <br/>                                                        |
| [**Rejournaliser**](systemmonitor-relog.md)                         | Rejournalise les données de compteur dans un nouveau fichier. Vous pouvez également utiliser cette méthode pour spécifier un nouveau type de fichier et réduire le nombre d’échantillons contenus dans le fichier journal.<br/> |
| [**Initialisation**](systemmonitor-reset.md)                         | Supprime tous les objets [**CounterItem**](counteritem.md) de l’objet de collection de **compteurs** .<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Enregistre les valeurs de compteur de la vue du graphique dans un fichier journal.<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | Mettre à l’échelle les valeurs de compteur pour les adapter au graphique.<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | Définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | Actualise le contenu des fenêtres du moniteur système.<br/>                                                                                                         |



 

### <a name="properties"></a>Propriétés

L’objet **systemmonitor** a ces propriétés.



| Propriété                                                                                | Description                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Apparence**](systemmonitor-appearance.md)<br/>                               | Récupère ou définit l’apparence du contrôle pour inclure ou omettre les effets d’affichage en trois dimensions.<br/>                                                                                                                        |
| [**BackColor**](systemmonitor-backcolor.md)<br/>                                 | Récupère ou définit la couleur d’arrière-plan du graphique et des vues de rapport.<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | Récupère ou définit la couleur d’arrière-plan du contrôle.<br/>                                                                                                                                                                       |
| [**BorderStyle**](systemmonitor-borderstyle.md)<br/>                             | Récupère ou définit le style de bordure du contrôle.<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | Récupère ou définit une valeur qui détermine si le graphique linéaire défile dans la vue.<br/>                                                                                                                                             |
| [**Counters**](systemmonitor-counters.md)<br/>                                   | Récupère la collection d’objets [**CounterItem**](counteritem.md) .<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | Récupère ou définit le nombre de points de données affichés dans un graphique linéaire.<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | Récupère ou définit la source des données du compteur de performance.<br/>                                                                                                                                                                |
| [**DisplayType**](systemmonitor-displaytype.md)<br/>                             | Récupère ou définit le type de graphique utilisé pour représenter graphiquement les données du compteur de performance.<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | Récupère ou définit une valeur qui détermine si SYSMON utilise le regroupement de chiffres lors de l’affichage de valeurs numériques.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Récupère ou définit une valeur qui détermine si une info-bulle est affichée lorsque la souris pointe sur un compteur dans l’une des vues du graphique.<br/>                                                                                             |
| [**Police**](systemmonitor-font.md)<br/>                                           | Récupère ou définit la police utilisée dans le contrôle.<br/>                                                                                                                                                                              |
| [**CouleurTexte**](systemmonitor-forecolor.md)<br/>                                 | Récupère ou définit la couleur du texte qui apparaît dans le contrôle.<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | Récupère ou définit le titre du graphique.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Récupère ou définit la couleur des lignes de la grille utilisées dans le graphique.<br/>                                                                                                                                                             |
| [**Surlignage**](systemmonitor-highlight.md)<br/>                                 | Récupère ou définit une valeur indiquant si les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique.<br/>                                                                                                               |
| [**Nomdefichierjournal**](systemmonitor-logfilename.md)<br/>                             | Obsolète. Récupère ou définit le nom d’un fichier journal à utiliser comme source des valeurs de compteur affichées dans le moniteur système.<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | Collection d’un ou de plusieurs fichiers journaux à utiliser comme source des valeurs de compteur affichées dans le moniteur système.<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | Récupère l’horodatage de la valeur de compteur la plus ancienne d’un compteur de votre collection de compteurs qui a été enregistré dans les fichiers journaux.<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | Récupère l’horodatage de la dernière valeur de compteur d’un compteur de votre collection de compteurs qui a été enregistré dans les fichiers journaux.<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | Récupère ou définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | Récupère ou définit la date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Récupère ou définit une valeur indiquant si le contenu du moniteur système est mis à jour manuellement ou automatiquement à des intervalles spécifiés.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Récupère ou définit la valeur maximale de l’axe vertical (Y) du graphique.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Récupère ou définit la valeur minimale de l’axe vertical (Y) du graphique.<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | Récupère ou définit une valeur qui détermine si plusieurs instances d’un compteur peuvent être surveillées.<br/>                                                                                                                          |
| [**Seulement**](systemmonitor-readonly.md)<br/>                                   | Récupère ou définit une valeur qui détermine si un utilisateur peut modifier les valeurs de propriété du contrôle.<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Récupère ou définit une valeur qui détermine si les vues de l’histogramme et du rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée de l’échantillonnage, telle que la valeur de compteur moyenne ou minimale.<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Récupère ou définit une valeur qui détermine si les lignes de grille horizontales sont affichées dans le graphique.<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | Récupère ou définit une valeur qui détermine si la légende est affichée.<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | Récupère ou définit une valeur qui détermine si les étiquettes d’échelle sont affichées sur l’axe vertical du graphique.<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Récupère ou définit une valeur qui détermine si l’axe horizontal (X) de la vue du graphique contient des étiquettes.<br/>                                                                                                                      |
| [**ShowToolbar**](systemmonitor-showtoolbar.md)<br/>                             | Récupère ou définit une valeur qui détermine si la barre d’outils est affichée sur le contrôle.<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | Récupère ou définit une valeur qui détermine si la barre de valeur (l’ensemble de valeurs statistiques sous le graphique) est affichée sur le contrôle.<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | Récupère ou définit une valeur qui détermine si les lignes verticales du quadrillage s’affichent dans le graphique.<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | Récupère ou définit le nom de la source de données ODBC.<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | Récupère ou définit le nom convivial du jeu de journaux.<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | Récupère ou définit la couleur de la barre d’heure (la barre verticale qui se déplace dans la fenêtre du graphique pour indiquer le passage de chaque intervalle d’échantillonnage dans la vue du graphique linéaire).<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Récupère ou définit la durée d’attente de l’exécution de SYSMON avant la prochaine mise à jour du graphique ou du rapport.<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | Récupère ou définit l’étiquette de l’axe vertical (Y) du graphique.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





