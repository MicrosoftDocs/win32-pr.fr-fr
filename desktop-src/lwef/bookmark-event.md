---
title: Signet, événement
description: Signet, événement
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976709"
---
# <a name="bookmark-event"></a>Signet, événement

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsqu’un signet dans une chaîne de texte vocal que votre application a définie est activé.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

Signet du **sous-** *agent* \_  **(ByVal** - *BookmarkID * * *)**



| Partie         | Description                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Entier long identifiant le numéro de signet. |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Pour spécifier un événement Bookmark, utilisez la méthode [**Speak**](speak-method.md) avec une balise **MRK** dans le texte fourni. Pour plus d’informations sur les balises, consultez balises de sortie vocale.

 

 




