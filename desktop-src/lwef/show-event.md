---
title: Afficher l’événement
description: Afficher l’événement
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b126c7726f8b8ed3ce1e83162cf41ad3223700630167448ff8a7655817a0604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975738"
---
# <a name="show-event"></a>Afficher l’événement

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsqu’un caractère est affiché.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent * * * \_ Show (ByVal* *  *CharacterID*, **ByVal** *cause * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère affiché en tant que chaîne.                                                                                                                                                                                                                          |
| *Cause*       | Retourne une valeur qui indique ce qui a provoqué l’affichage du caractère. 2 l’utilisateur a affiché le caractère (à l’aide du menu ou de la commande vocale).<br/> 4 votre application cliente affichait le caractère.<br/> 6 une autre application cliente affichait le caractère.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Le serveur envoie cet événement à tous les clients du caractère. Pour interroger l’état actuel du caractère, utilisez la propriété [**visible**](visible-property.md) .

### <a name="see-also"></a>Voir aussi

[**Masquer l’événement**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





