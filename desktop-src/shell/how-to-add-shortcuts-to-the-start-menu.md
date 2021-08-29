---
description: Pour ajouter un élément au sous-menu programmes, procédez comme suit.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Comment ajouter des raccourcis au menu Démarrer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8c31f8180f4bd0d3b8aa8252d7c3f1fedc4238bb5320f8179f3a4fd4b497b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969428"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Comment ajouter des raccourcis au menu Démarrer

Pour ajouter un élément au sous-menu **programmes** , procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Créez un [lien de Shell](./links.md) à l’aide de l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .

### <a name="step-2"></a>Étape 2 :

Obtenez l’emplacement du dossier programmes à l’aide de la fonction [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , en passant les [**\_ programmes FOLDERID**](knownfolderid.md).

### <a name="step-3"></a>Étape 3 :

Ajoutez le lien de l’interpréteur de commandes au dossier programmes. Vous pouvez également créer un dossier dans le dossier programmes et ajouter le lien vers ce dossier.

 

 
