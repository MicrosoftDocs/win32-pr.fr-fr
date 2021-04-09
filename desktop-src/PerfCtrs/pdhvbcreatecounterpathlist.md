---
description: La fonction PdhVbCreateCounterPathList affiche la boîte de dialogue exploration des compteurs de performance, qui permet à l’utilisateur de sélectionner plusieurs compteurs de performances. Chaque chemin de compteur sélectionné doit ensuite être lu à l’aide de la fonction PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865117"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>PdhVbCreateCounterPathList fonction)

La fonction **PdhVbCreateCounterPathList** affiche la boîte de dialogue exploration des compteurs de performance, qui permet à l’utilisateur de sélectionner plusieurs compteurs de performances. Chaque chemin de compteur sélectionné doit ensuite être lu à l’aide de la fonction [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbCreateCounterPathList ( \_ ByVal DetailLevel As long, \_ ByVal CaptionString As String \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Types de compteurs à afficher dans la boîte de dialogue. Utilisez l’une des valeurs suivantes.



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

## <a name="return-value"></a>Valeur retournée

La fonction retourne le nombre de chemins d’accès aux compteurs sélectionnés par l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




