---
title: Attributs de pointeur appliqués au paramètre
description: Chaque attribut de pointeur (\ Ref \, \ unique \ et \ PTR \) a des caractéristiques qui affectent l’allocation de mémoire. Le tableau suivant récapitule ces caractéristiques.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcc6649dc663d7b029a7d7f345719330719d2eb19b6b7a63fa02797c17df16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927494"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Attributs de pointeur appliqués au paramètre

Chaque attribut de pointeur ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [unique](/windows/desktop/Midl/unique) \] et \[ [ptr](/windows/desktop/Midl/ptr) \] ) a des caractéristiques qui affectent l’allocation de mémoire. Le tableau suivant récapitule ces caractéristiques.



| Attribut de pointeur       | Client                                                                                                                                                                                                            | Serveur                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Référence ( \[ **ref** \] ) | L’application cliente doit allouer.                                                                                                                                                                                 | Gestion spéciale nécessaire pour les pointeurs de niveau nontop en **\[ sortie \]** seule. |
| Unique ( \[ **unique** \] ) | Si un paramètre est, l’application cliente doit allouer ; s’il est incorporé, peut avoir la valeur null. Si vous remplacez la valeur NULL par une valeur non null, le stub client est alloué. le passage de la valeur non null à la valeur NULL peut entraîner l’orphelin.<br/> |                                                                     |
| Full ( \[ **ptr** \] )      | Si un paramètre est, l’application cliente doit allouer ; s’il est incorporé, peut avoir la valeur null. Si vous remplacez la valeur NULL par une valeur non null, le stub client est alloué. le passage de la valeur non null à la valeur NULL peut entraîner l’orphelin.<br/> |                                                                     |



 

L’attribut **\[ Ref \]** indique que le pointeur pointe vers une mémoire valide. Par définition, l’application cliente doit allouer toute la mémoire requise par les pointeurs de référence.

Le pointeur unique peut passer de la valeur null à la valeur non null. Si le pointeur unique passe de null à non null, une nouvelle mémoire est allouée sur le client. Si le pointeur unique passe de non null à null, l’orphelin peut en résulter. Pour plus d’informations, consultez [orphelins de mémoire](memory-orphaning.md).

 

