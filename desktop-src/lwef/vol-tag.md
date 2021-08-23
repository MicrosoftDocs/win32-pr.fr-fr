---
title: Indicateur vol
description: Indicateur vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d03b7bb536ada8dc783e1506ba4bedfd54c6b5698e1aa68dfe55fd1f939d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035977"
---
# <a name="vol-tag"></a>Indicateur vol

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Définit le volume de base de la sortie vocale.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**\\ Vol =**_nombre_*_\\_*



| Partie     | Description                                                         |
|----------|---------------------------------------------------------------------|
| *number* | Volume de base de référence : 0 correspond au silence et 65535 au volume maximal. |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Le paramètre de volume affecte les canaux gauche et droit. Vous ne pouvez pas définir le volume de chaque canal séparément. Cette balise est prise en charge uniquement pour la sortie générée par TTS.

 

 




