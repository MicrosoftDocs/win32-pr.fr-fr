---
title: Ressource HTML
description: Définit un fichier HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menus de ressources HTML et autres ressources
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947feb790b5fbee628c846f88595b1ae25db4cfddedbbab223fd05513560d63e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687771"
---
# <a name="html-resource"></a>Ressource HTML

Définit un fichier HTML.

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits identifiant la ressource.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier HTML. Il doit s’agir d’un chemin d’accès complet ou relatif si le fichier ne se trouve pas dans le répertoire de travail actuel. Le chemin d’accès doit être une chaîne entre guillemets.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple suivant définit une ressource HTML :

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




