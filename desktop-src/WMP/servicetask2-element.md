---
title: Élément ServiceTask2
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément ServiceTask2 représente le deuxième volet des tâches du magasin en ligne.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- Élément ServiceTask2 lecteur Windows Media
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36052dabc1be7f2925f5185239faa602b8633fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540081"
---
# <a name="servicetask2-element"></a>Élément ServiceTask2

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **ServiceTask2** représente le deuxième volet des tâches du magasin en ligne.

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributs



| Terme                                                                                                                             | Description                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)<br/> | URL de la page Web affichée par le lecteur Windows Media.<br/> |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément                       |
|-----------------|-------------------------------|
| Éléments parents | **ServiceInfo**               |
| Éléments enfants  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Notes

**ServiceTask1** est considéré comme le volet principal des tâches pour engager des activités commerciales. Il s’agit du volet des tâches qui s’affiche lorsque l’utilisateur choisit d’acheter de la musique. Utilisez **ServiceTask2** pour les autres activités du magasin en ligne.

> [!Note]  
> Le lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages Web. Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches. Le lecteur Windows Media 11 n’a qu’un seul volet de tâches, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** . le lecteur Windows Media 11 ignore les éléments **ServiceTask2** et **ServiceTask3** .

 

Les volets des tâches magasins en ligne partagent une seule instance de navigateur. Cela signifie que vous ne devez pas écrire de code de script dans votre page Web que vous prévoyez de continuer à exécuter quand l’utilisateur quitte la tâche de service actuelle.

Lorsque l’utilisateur bascule les volets de tâches, le lecteur Windows Media stocke les cookies d’URL et de session. Lorsque l’utilisateur revient au volet de tâches, le lecteur restaure l’URL et les cookies. Si l’utilisateur choisit d’utiliser un autre magasin en ligne, l’URL et les données de session sont effacées.

Le tableau suivant détaille les paramètres envoyés avec la demande d’URL. D’autres peuvent être présents à des fins de compatibilité héritée.



| Nom         | Valeur                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | ID d’emplacement géographique Windows. L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration. |
| *locale*     | ID de paramètres régionaux du lecteur Windows Media.                                                                                                                                     |
| *UserLocale* | ID de paramètres régionaux Windows. Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.        |
| *version*    | Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





