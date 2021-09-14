---
description: Le sous-système POSIX doit pouvoir traduire tout identificateur de sécurité (SID) qu’il rencontre dans une valeur 32 bits, appelée ID POSIX.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Mappage d’identificateurs POSIX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013601"
---
# <a name="mapping-posix-identifiers"></a>Mappage d’identificateurs POSIX

Le sous-système POSIX doit pouvoir traduire tout [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qu’il rencontre dans une valeur 32 bits, appelée *ID POSIX*. En outre, il doit être en mesure de classer l’ID comme un ID d’utilisateur ou un ID de groupe. Pour comprendre comment ce mappage est accompli, commençons par examiner les SID qui doivent être mappés.

Les SID comportent deux composants, le SID du domaine et l’ID relatif du compte dans le domaine. Par exemple, dans le SID S-1-518364-21-43-8, le dernier numéro, 8, est l’ID relatif du compte (RID) et S-1-518364-21-43 est le SID du domaine.

Les informations de domaine sont stockées dans les objets [**trustedDomain**](trusteddomain-object.md) . Une partie des informations stockées dans un objet **trustedDomain** est un décalage d’ID POSIX à utiliser pour les SID au sein de ce domaine. Par exemple, supposons qu’un **trustedDomain** est défini comme suit :

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

Les ID POSIX pour les comptes de ce domaine sont générés en ajoutant 0x130000 à l’ID relatif du compte. Ainsi, l’ID POSIX correspondant au SID S-1-518364-21-43-8 est 0x130008.

Toutes les traductions d’ID POSIX ne font pas appel à un objet [**trustedDomain**](trusteddomain-object.md) . Le tableau suivant répertorie les SID mappés à l’aide de valeurs de décalage connues.



| Source                                              | Décalage de l’ID POSIX |
|-----------------------------------------------------|-----------------|
| Sid du domaine intégré                       | 0x20000         |
| Sid du domaine du compte                        | 0x30000         |
| Sid du domaine principal (sur les stations de travail uniquement) | 0x40000         |



 

Enfin, un autre ensemble de sid, SID d’ouverture de session, nécessite un traitement spécial. ces valeurs sont affectées par le processus d’ouverture de session Windows pour chaque ouverture de session et se présentent sous la forme S-1-5-5-X-Y, où X et Y sont traités comme un seul \_ entier volumineux qui est incrémenté pour chaque session d’ouverture de session. Ces SID sont mappés à la constante ID POSIX 0xFFF. Pour mapper l’ID POSIX 0xFFF, vous pouvez traduire n’importe quel [*identificateur de connexion*](/windows/desktop/SecGloss/l-gly) adapté à la situation, ou vous pouvez utiliser par défaut S-1-5-5-0-0. (Par exemple, si un utilisateur POSIX applique la protection à un objet et spécifie FFFx, il est préférable de remplacer l’identificateur d’ouverture de session de cet utilisateur par la seule attribution de S-1-5-5-0-0.)

 

 
