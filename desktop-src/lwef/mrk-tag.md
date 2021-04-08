---
title: Balise MRK
description: Balise MRK
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673206"
---
# <a name="mrk-tag"></a>Balise MRK

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Définit un signet dans le texte parlé.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**\\MRK =***nombre***\\**



| Partie     | Description                                        |
|----------|----------------------------------------------------|
| *number* | Valeur entière de type long qui identifie le signet. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Quand le serveur traite un signet, il génère un événement Bookmark. Vous devez spécifier un nombre supérieur à zéro (0) et différent de 2147483647 ou 2147483646.

 

 




