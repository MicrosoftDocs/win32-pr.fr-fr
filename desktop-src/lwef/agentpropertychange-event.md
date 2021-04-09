---
title: Événement AgentPropertyChange
description: Événement AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028992"
---
# <a name="agentpropertychange-event"></a>Événement AgentPropertyChange

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque l’utilisateur modifie une propriété dans la fenêtre Options de caractères avancés.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent. * * * AgentPropertyChange**

</dd> </dl>

### <a name="remarks"></a>Notes

Cet événement indique que l’utilisateur a modifié et appliqué une propriété incluse dans la fenêtre Options de caractères avancés.

Dans votre code, pour gérer cet événement, vous pouvez interroger les paramètres de propriété spécifiques des objets [AudioOutput](the-audiooutput-object.md) ou [SpeechInput](the-speechinput-object.md) .

### <a name="see-also"></a>Voir aussi

[**Événement DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




