---
title: Balise CTX
description: Balise CTX
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7071994e741cb7dfd1147f163f0d7ef6299ec0dcb9d568ad068251d5a9436809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726098"
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

### <a name="remarks"></a>Remarques

Cette balise est prise en charge uniquement pour la sortie générée par TTS. La plage de valeurs du paramètre peut varier selon le moteur TTS installé.

 

 





