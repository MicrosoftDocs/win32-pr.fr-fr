---
description: Cette classe est la classe parente pour les événements d’erreur de page. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: Classe PageFault_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd8adfa698975f7661abdbd849136d04049b5539ff3fed3b52b61660791add0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900749"
---
# <a name="pagefault_v2-class"></a>\_Classe PageFault v2

Cette classe est la classe parente pour les événements d’erreur de page.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **PageFault \_ v2** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer tous les événements d’erreur de page dans une session de journalisation du noyau NT, spécifiez l’indicateur de  **\_ \_ \_ \_ \_ défaillance de page mémoire** de l’indicateur de trace d’événements dans le membre EnableFlags d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Vous pouvez également spécifier les indicateurs suivants :

-   **erreur de mémoire de l’indicateur de trace d’événements \_ \_ \_ \_ \_**
-   **indicateur de suivi d’événement- \_ \_ \_ \_ allocation virtuelle**

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour tous les événements d’erreur de page en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**PageFaultGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement de mémoire réel lors de la consommation d’événements.



| Type d'événement                                                     | Description                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Type de suivi d’événement \_ \_ mm \_ Cow (la valeur de type d’événement est 12)<br/> | Événement de copie sur écriture. La classe [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF définit les données d’événement pour cet événement. avant Windows Vista, la classe MOF [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) définit l’événement.     |
| \_Type de suivi d’événement \_ \_ mm \_ DZF (la valeur de type d’événement est 11)<br/> | Événement d’erreur de la demande zéro. La classe [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF définit les données d’événement pour cet événement. avant Windows Vista, la classe MOF [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) définit l’événement. |
| \_Type de suivi d’événement \_ \_ mm \_ GPF (la valeur de type d’événement est 13)<br/> | Événement d’erreur de page de garde. La classe [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF définit les données d’événement pour cet événement. avant Windows Vista, la classe MOF [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) définit l’événement.  |
| \_Type de suivi d’événement \_ \_ mm \_ HPF (la valeur de type d’événement est 14)<br/> | Événement d’erreur de page matérielle. La classe [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF définit les données d’événement pour cet événement. avant Windows Vista, la classe MOF [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) définit l’événement.   |
| Type de suivi d’événement \_ \_ \_ mm \_ TF (la valeur de type d’événement est 10)<br/>  | Événement d’erreur de transition. La classe [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF définit les données d’événement pour cet événement. avant Windows Vista, la classe MOF [**PageFault \_ TransitionFault**](pagefault-transitionfault.md) définit l’événement.  |
| \_Type de suivi d’événement \_ \_ mm \_ AV (la valeur de type d’événement est 15)<br/>  | Événement de violation d’accès. La classe [**PageFault \_ TypeGroup1**](pagefault-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                                                           |
| Valeur de type d’événement, 32                                           | Événement d’erreur de page matérielle. La classe [**PageFault \_ HardFault**](pagefault-hardfault.md) MOF définit les données d’événement pour cet événement.                                                                                                                               |
| Valeur de type d’événement, 105                                          | Chargement de l’image dans l’événement de fichier d’échange. La classe [**PageFault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) MOF définit les données d’événement pour cet événement.                                                                                                          |
| Valeur de type d’événement, 98                                           | Événement d’allocation virtuelle. La classe de la classe MOF [**VirtualAlloc**](pagefault-virtualalloc.md) définit les données d’événement pour cet événement.                                                                                                                                |
| Valeur de type d’événement, 99                                           | Événement libre virtuel. La classe de la classe MOF [**VirtualAlloc**](pagefault-virtualalloc.md) définit les données d’événement pour cet événement.                                                                                                                                      |



 

Vous pouvez utiliser les membres **ProcessID** et **ThreadID** de [**l' \_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier le processus ou le thread défaillant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 
