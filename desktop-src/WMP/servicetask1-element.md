---
title: Élément ServiceTask1
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément ServiceTask1 représente le premier volet des tâches du magasin en ligne.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- élément ServiceTask1 Lecteur Windows Media
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fc22e01329728935e2953b5be7a3a1042cee00da3a3b9756915de2aeafe9b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995409"
---
# <a name="servicetask1-element"></a>Élément ServiceTask1

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **ServiceTask1** représente le premier volet des tâches du magasin en ligne.

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributs



| Terme                                                                                                                             | Description                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)<br/> | URL de la page web que Lecteur Windows Media affiche.<br/> |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément                       |
|-----------------|-------------------------------|
| Éléments parents | **ServiceInfo**               |
| Éléments enfants  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Remarques

**ServiceTask1** est considéré comme le volet principal des tâches pour engager des activités commerciales. Il s’agit du volet des tâches qui s’affiche lorsque l’utilisateur choisit d’acheter de la musique.

> [!Note]  
> Lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages web. Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches. Lecteur Windows Media 11 n’a qu’un seul volet de tâches, représenté par **ServiceTask1**, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** .

 

Les volets des tâches du magasin en ligne partagent une seule instance de navigateur. Cela signifie que vous ne devez pas écrire de code de script dans votre page Web que vous prévoyez de continuer à exécuter quand l’utilisateur quitte la tâche de service actuelle.

lorsque l’utilisateur bascule les volets de tâches, Lecteur Windows Media stocke les cookies d’URL et de session. Lorsque l’utilisateur revient au volet de tâches, le lecteur restaure l’URL et les cookies. Si l’utilisateur choisit d’utiliser un autre magasin en ligne, l’URL et les données de session sont effacées.

Le tableau suivant détaille les paramètres envoyés avec la demande d’URL. D’autres peuvent être présents à des fins de compatibilité héritée.



| Nom         | Valeur                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | Windows l’ID d’emplacement géographique. L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration. |
| *locale*     | ID de paramètres régionaux Lecteur Windows Media.                                                                                                                                     |
| *UserLocale* | ID de paramètres régionaux Windows. Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.        |
| *version*    | Lecteur Windows Media numéro de version en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

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

 

 





