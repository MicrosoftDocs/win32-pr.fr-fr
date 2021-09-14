---
title: Signet, événement
description: Signet, événement
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012394"
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

### <a name="remarks"></a>Notes

Pour spécifier un événement Bookmark, utilisez la méthode [**Speak**](speak-method.md) avec une balise **MRK** dans le texte fourni. Pour plus d’informations sur les balises, consultez balises de sortie vocale.

 

 




