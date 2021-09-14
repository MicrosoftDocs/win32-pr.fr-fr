---
description: La fonction PdhVbGetOneCounterPath affiche une boîte de dialogue qui permet à l’utilisateur de parcourir les compteurs de performance disponibles et de sélectionner un compteur.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009187"
---
# <a name="pdhvbgetonecounterpath-function"></a>PdhVbGetOneCounterPath fonction)

La fonction **PdhVbGetOneCounterPath** affiche une boîte de dialogue qui permet à l’utilisateur de parcourir les compteurs de performance disponibles et de sélectionner un compteur. Le compteur sélectionné est retourné dans la variable *PathString* . La variable *PathString* doit être dimensionnée et initialisée avant que cette fonction soit appelée, et la taille dimensionnée doit être indiquée par la variable *PathLength* .

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbGetOneCounterPath ( \_ ByVal PathString As String, \_ ByVal PathLength As long, \_ ByVal DetailLevel As long, \_ ByVal CaptionString As String \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*PathString* 
</dt> <dd>

Variable de chaîne initialisée utilisée pour recevoir le chemin d’accès au compteur sélectionné par l’utilisateur.

</dd> <dt>

*PathLength* 
</dt> <dd>

Longueur du PathString initialisé.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Types de compteurs à afficher dans la boîte de dialogue. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                               | Signification                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**détail des performances- \_ \_ avancé**</dt> </dl> | Compteurs que l’utilisateur avancé est susceptible de comprendre, en plus des compteurs utilisateur novice.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**\_expert en détail des performances \_**</dt> </dl>       | Les compteurs que l’utilisateur expérimenté et le développeur de logiciels peuvent comprendre, en plus des compteurs pour les utilisateurs débutants et expérimentés.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**\_novice détaillé sur les performances \_**</dt> </dl>       | Seuls les compteurs que l’utilisateur novice est susceptible de comprendre.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**\_Assistant détail des performances \_**</dt> </dl>       | Tous les compteurs du système.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variable de chaîne qui contient le texte qui sera affiché dans la barre de légende de la boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La fonction retourne le nombre de caractères écrits dans la mémoire tampon *PathString* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




