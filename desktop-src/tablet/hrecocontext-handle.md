---
description: Un descripteur HRECOCONTEXT est utilisé pour ajouter de l’encre au contexte, effectuer la reconnaissance de l’encre (de façon synchrone ou asynchrone), récupérer le résultat de la reconnaissance et récupérer d’autres.
ms.assetid: 509188e2-28af-4915-bc76-ee451133398f
title: Handle HRECOCONTEXT (Récapitulatifis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef2b6f629587de84f831fd32a31f42a208c024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862734"
---
# <a name="hrecocontext-handle"></a>Handle HRECOCONTEXT

Un descripteur **HRECOCONTEXT** est utilisé pour ajouter de l’encre au contexte, effectuer la reconnaissance de l’encre (de façon synchrone ou asynchrone), récupérer le résultat de la reconnaissance et récupérer d’autres.

La raison principale de l’existence de handles de contexte de reconnaissance consiste à faire la distinction entre les entrées d’entrée manuscrite. Par exemple, vous pouvez créer une application avec deux fenêtres, l’utilisateur étant en mesure d’écrire dans l’une ou l’autre fenêtre. Vous ne souhaitez pas que l’encre de la première fenêtre ne soit mélangée à l’encre de la deuxième fenêtre lorsque vous demandez au module de reconnaissance de reconnaître l’encre de l’une des fenêtres. Dans ce type d’application, vous créez deux contextes de reconnaissance (un pour chaque fenêtre) et vous ajoutez des traits qui arrivent dans la fenêtre 1 dans le contexte de reconnaissance 1 et les traits de la fenêtre 2 dans le contexte de reconnaissance 2. Pour retourner les résultats de la reconnaissance, appelez le processus sur le contexte de reconnaissance 1 ou le contexte de reconnaissance 2 selon que vous souhaitez ou non les résultats pour la fenêtre 1 ou 2.

Le handle de contexte du module de reconnaissance peut être tout ce que vous souhaitez. Mais en général, il s’agit d’un index dans un tableau global de structures. Les structures peuvent contenir tous les traits qui ont été entrés et toutes les variables que le module de reconnaissance utilise pour cette partie d’encre particulière (par exemple, votre structure de treillis interne ou l’état actuel de reconnaissance). Une structure peut contenir toutes les informations dont le module de reconnaissance a besoin et utilise pour une partie de l’encre particulière.

Pour récupérer un handle **HRECOCONTEXT** , appelez la fonction [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .


```C++
typedef HANDLE HRECOCONTEXT;
```



## <a name="remarks"></a>Notes

Les fonctions **HRECOCONTEXT** sont les suivantes :



| Fonction                                                            | Description                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStroke**](/windows/desktop/api/recapis/nf-recapis-addstroke)                                      | Ajoute un trait d’encre au contexte du module de reconnaissance.<br/>                                                                                                                                                                                                    |
| [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange)                          | Empêche le module de reconnaissance de traiter l’encre car un nouveau trait est ajouté ou supprimé.<br/>                                                                                                                                                         |
| [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext)                                | Crée un contexte de module de reconnaissance qui contient les mêmes paramètres que le d’origine. Le nouveau contexte de module de reconnaissance n’inclut pas les résultats d’encre ou de reconnaissance de l’original.<br/>                                                                        |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)             | Indique qu’aucune entrée manuscrite supplémentaire ne sera ajoutée au contexte.<br/>                                                                                                                                                                                         |
| [**GetAlternateList**](/previous-versions/windows/desktop/legacy/ms698163(v=vs.85))                        | Retourne une liste d’alternatives pour la meilleure chaîne de résultat.<br/>                                                                                                                                                                                         |
| [**GetBestAlternate**](/previous-versions/windows/desktop/legacy/ms699575(v=vs.85))                        | Retourne un pointeur de [handle HRECOALT](hrecoalt-handle.md) pour le meilleur résultat alternatif.<br/>                                                                                                                                                         |
| [**GetBestResultString**](/windows/desktop/api/recapis/nf-recapis-getbestresultstring)                  | Retourne la meilleure chaîne de résultat.<br/>                                                                                                                                                                                                                  |
| [**GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)            | Retourne la liste des propriétés prises en charge par le module de reconnaissance.<br/>                                                                                                                                                                                            |
| [**GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)          | Retourne une valeur de propriété spécifiée à partir du contexte de module de reconnaissance.<br/>                                                                                                                                                                                  |
| [**GetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)          | Retourne une liste de plages de points Unicode activée sur le contexte.<br/>                                                                                                                                                                                   |
| [**GetGuide**](/windows/desktop/api/recapis/nf-recapis-getguide)                                        | Retourne le repère utilisé pour l’entrée boxed ou lineed.<br/>                                                                                                                                                                                                 |
| [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr)                              | Retourne un pointeur vers le treillis pour les résultats actuels.<br/>                                                                                                                                                                                        |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) | Retourne une valeur qui indique si un mot, une date, une heure, un nombre ou un autre texte passé est contenu dans le dictionnaire.<br/>                                                                                                               |
| [**Processus**](/windows/desktop/api/recapis/nf-recapis-process)                                          | Effectue la reconnaissance de l’encre de façon synchrone.<br/>                                                                                                                                                                                                          |
| [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext)                                | Supprime l’encre et les résultats de reconnaissance actuels du contexte.<br/>                                                                                                                                                                                |
| [**SetCACMode**](/windows/desktop/api/recapis/nf-recapis-setcacmode)                                    | Spécifie le mode de saisie semi-automatique de caractères pour la reconnaissance de caractères ou de mots.<br/>                                                                                                                                                                         |
| [**SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)          | Ajoute une propriété au contexte de module de reconnaissance. Si une propriété existe déjà, sa valeur est modifiée.<br/>                                                                                                                                                  |
| [**SetEnabledUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)          | Active une ou plusieurs plages de points Unicode sur le contexte.<br/>                                                                                                                                                                                         |
| [**SetFactoid**](/windows/desktop/api/recapis/nf-recapis-setfactoid)                                    | Définit le Factoid qu’un module de reconnaissance utilise pour contraindre sa recherche au résultat.<br/>                                                                                                                                                                       |
| [**SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)                                        | Définit la façon dont le module de reconnaissance interprète l’encre et détermine la chaîne de résultat.<br/>                                                                                                                                                                     |
| [**SetGuide**](/windows/desktop/api/recapis/nf-recapis-setguide)                                        | Définit le repère à utiliser pour l’entrée boxed ou lineed.<br/>                                                                                                                                                                                                  |
| [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext)                            | Fournit les chaînes de texte qui précèdent et suivent le texte contenu dans le contexte du module de reconnaissance. Pour les reconnaissances de caractères d’Extrême-Orient, la fonction [**SetTextContext**](/windows/desktop/api/recapis/nf-recapis-settextcontext) fournit des caractères plutôt que des chaînes de texte.<br/> |
| [**SetWordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)                                  | Définit la liste de mots pour le contexte de module de reconnaissance actuel à reconnaître.<br/>                                                                                                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Récapitulatif</dt> </dl> |



 

