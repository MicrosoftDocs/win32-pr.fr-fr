---
title: Masquer l’événement
description: Masquer l’événement
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02974d1d66a22eab24c93fc5c9d29b9c2d0e604082fef9f4f0583ebcf7354576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062059"
---
# <a name="hide-event"></a>Masquer l’événement

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsqu’un caractère est masqué.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent * * * \_ Hide (* *  **ByVal** *CharacterID*, **ByVal** *cause * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère masqué sous forme de chaîne.                                                                                                                                                                                                                                                                                                                                                               |
| *Cause*       | Retourne une valeur qui indique ce qui a provoqué le masquage du caractère. 1 utilisateur a masqué le caractère en sélectionnant la commande dans le menu contextuel de l’icône de barre des tâches du caractère ou en utilisant l’entrée vocale.<br/> 3 votre application cliente a masqué le caractère.<br/> 5 une autre application cliente a masqué le caractère.<br/> 7 l’utilisateur a masqué le caractère en sélectionnant la commande dans le menu contextuel du caractère.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Le serveur envoie cet événement à tous les clients du caractère. Pour interroger l’état actuel du caractère, utilisez la propriété [**visible**](visible-property.md) .

### <a name="see-also"></a>Voir aussi

[**Afficher l’événement**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





