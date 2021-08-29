---
title: Événement AgentPropertyChange
description: Événement AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accafc89fbcd9f29dd7327cc4561c0375f773abe01077bab7cbfa24653f6106d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752690"
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

### <a name="remarks"></a>Remarques

Cet événement indique que l’utilisateur a modifié et appliqué une propriété incluse dans la fenêtre Options de caractères avancés.

Dans votre code, pour gérer cet événement, vous pouvez interroger les paramètres de propriété spécifiques des objets [AudioOutput](the-audiooutput-object.md) ou [SpeechInput](the-speechinput-object.md) .

### <a name="see-also"></a>Voir aussi

[**Événement DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




