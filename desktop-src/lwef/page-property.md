---
title: Page, propriété
description: Page, propriété
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379924"
---
# <a name="page-property"></a>Page, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la page affichée dans la fenêtre de la feuille de propriétés de l’agent Microsoft.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent * * *.* *  \[  =  *Chaîne* PropertySheet.page\]



| Partie     | Description                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Expression de chaîne avec l’une des valeurs suivantes. **« Parole »** Affiche la page d’entrée vocale.<br/> **« Sortie »** Affiche la page sortie.<br/> **« Copyright »** Affiche la page de copyright.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si aucun moteur de reconnaissance vocale n’est installé, la définition de la valeur **« parole »** de la **page** n’a aucun effet. En outre, la propriété **visible** de la fenêtre doit avoir la valeur **true** pour permettre à l’utilisateur d’afficher la page.

> [!Note]  
> L’utilisateur peut remplacer cette propriété.

 

 

 





