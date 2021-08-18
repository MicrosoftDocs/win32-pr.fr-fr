---
title: Énumération ViewContents
description: Utilisé par le contenu IResultsViewer pour indiquer ou définir le mode d’affichage du jeu de requêtes actuel.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- ViewContents, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829109"
---
# <a name="viewcontents-enumeration"></a>Énumération ViewContents

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Utilisé par [**IResultsViewer :: content**](-search-2x-iresultsviewer-contents.md) pour indiquer ou définir le mode d’affichage du jeu de requêtes actuel.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**
</dt> <dd>

Indique le type de contenu affiché dans l’affichage des résultats.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

Indique que le type de contenu affiché dans l’affichage des résultats est actuellement défini sur la vue de l’interpréteur de commandes.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Indique que le type de contenu affiché dans l’affichage des résultats est actuellement défini sur la vue du navigateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





