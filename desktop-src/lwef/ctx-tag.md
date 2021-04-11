---
title: Balise CTX
description: Balise CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029450"
---
# <a name="ctx-tag"></a>Balise CTX

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Définit le contexte du texte de sortie.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

\\**CTX** = *chaîne*\\



| Partie     | Description                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Chaîne spécifiant le contexte du texte qui suit, qui détermine la façon dont les symboles ou les abréviations sont prononcés.<br/> **« Address »**    Adresses et/ou numéros de téléphone.<br/> **« E-mail »**    Courrier électronique.<br/> Le contexte **« inconnu »** (par défaut) est inconnu.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Cette balise est prise en charge uniquement pour la sortie générée par TTS. La plage de valeurs du paramètre peut varier selon le moteur TTS installé.

 

 





