---
title: Formats des messages d’erreur et d’avertissement
description: Liste des formats de message d’erreur et de message d’avertissement MIDL.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- Erreurs MIDL, formats de message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cbe6e32109bbe8e4d40b7715c6463e16cd0c27fc77492f5044ce32a7fe57436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384415"
---
# <a name="error-and-warning-message-formats"></a>Formats des messages d’erreur et d’avertissement

Les erreurs de ligne de commande s’affichent au format suivant :

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

Le champ informations supplémentaires sur l’erreur fournit des informations spécifiques au contexte en fonction du message d’erreur. Par exemple, lorsqu’une erreur de déclaration de type non résolue se produit, le champ informations supplémentaires sur l’erreur affiche le nom du type qui n’a pas pu être résolu.

Les avertissements au moment de la compilation s’affichent au format suivant :

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Les erreurs au moment de la compilation s’affichent au format suivant :

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

Les informations de contexte facultatives font référence au contexte dans lequel l’erreur s’est produite. Elle est générée lorsque le compilateur MIDL découvre une erreur lors de l’analyse sémantique des signatures de type et de procédure. Le compilateur MIDL signale ces informations pour vous aider à trouver rapidement l’erreur dans le fichier IDL.

Les messages d’erreur système s’affichent au format suivant :

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Ce message est généré par une erreur inattendue. le numéro d’erreur hexadécimal est un identificateur d’erreur système Windows XP, Windows 2000, Windows NT, Windows 98 ou Windows 95. Vous pouvez trouver des informations supplémentaires dans Winerror. h ou Ntstatus. h. Pour plus d’informations sur le contournement des conditions qui ont provoqué cette erreur, consultez le texte d’erreur pour l' [Erreur du compilateur](compiler-errors.md) MIDL9008.

 

 




