---
title: Erreurs et avertissements du compilateur MIDL
description: Lors de l’utilisation du compilateur MIDL, les erreurs et les avertissements peuvent être provoqués par une utilisation incorrecte des commutateurs de ligne de commande ou par le contenu des fichiers IDL et ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL, référence
- MIDL du compilateur MIDL, Erreurs
- MIDL du compilateur, Erreurs
- Erreurs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f6c2dfd830a1240e2af107eb4a3f1799eafcd0de35ccec7f3756b3e9de5bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146402"
---
# <a name="midl-compiler-errors-and-warnings"></a>Erreurs et avertissements du compilateur MIDL

Lors de l’utilisation du compilateur MIDL, les erreurs et les avertissements peuvent être provoqués par une utilisation incorrecte des commutateurs de ligne de commande ou par le contenu des fichiers IDL et ACF. Si l’erreur est due à l’entrée incorrecte des commutateurs de ligne de commande, un message d’erreur ou d’avertissement peut spécifier le nom d’un ou plusieurs commutateurs du compilateur MIDL. Par exemple, vous pouvez inclure certains attributs ACF dans un fichier IDL lorsque vous utilisez le commutateur/de **\_ configuration d’application** , mais ce fichier IDL génère une erreur si vous compilez sans utiliser le commutateur/**app \_ config** .

Les erreurs dans les fichiers IDL et ACF se répartissent en deux catégories : les erreurs interceptées par le préprocesseur et les erreurs reconnues par le compilateur. Cette section répertorie les messages d’erreur du compilateur et du préprocesseur MIDL. Il décrit également leurs formats et leurs causes.

-   [Formats des messages d’erreur et d’avertissement](error-and-warning-message-formats.md)
-   [Erreurs de préprocesseur](preprocessor-errors.md)
-   [Erreurs du compilateur](compiler-errors.md)

 

 




