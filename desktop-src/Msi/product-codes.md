---
description: Le code du produit est un GUID qui est l’identification principale d’une application ou d’un produit.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Codes de produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209716"
---
# <a name="product-codes"></a>Codes de produit

Le code du produit est un GUID qui est l’identification principale d’une application ou d’un produit. Pour plus d’informations, consultez la propriété [**ProductCode**](productcode.md) . Si des modifications significatives ont été apportées à un produit, le code de produit doit également être modifié pour refléter cela. Toutefois, il n’est pas obligatoire que le code du produit soit modifié si les modifications apportées au produit sont relativement mineures.

Les versions 32 bits et 64 bits du package d’une application doivent avoir des codes de produit différents. Si un composant 32 bits d’une application est recompilé en un composant 64 bits, un nouveau code de produit doit être attribué.

Si un serveur exposé dans la [table PublishComponent](publishcomponent-table.md) est recompilé de 32 bits à 64 bits, il est également nécessaire de modifier le GUID de cette table afin que les clients 32 bits et 64 bits puissent identifier la catégorie de composants qualifiés appropriée. Dans ce cas, le code du produit doit également être modifié.

Notez que les lettres dans les GUID de code de produit doivent être en majuscules. Les utilitaires tels que GUIDGEN génèrent des GUID contenant des minuscules. Les minuscules dans ces GUID doivent être remplacées par des majuscules à utiliser comme code de produit ou code de package. Pour plus d’informations, consultez [modification du code du produit](changing-the-product-code.md).

Le code du package est un GUID identifiant un [*package*](p-gly.md)de Windows Installer particulier. Le code du package associe un fichier. msi à une application ou à un produit et peut également être utilisé pour la vérification des sources. Les codes de produit et de package ne sont pas interchangeables. Deux fichiers. msi non identiques ne doivent jamais avoir le même code de package. Bien qu’il soit courant d’expédier une application qui possède le même code de package et le même code de produit, les deux valeurs peuvent divergent lorsque l’application est mise à jour. Pour plus d’informations, consultez [codes de package](package-codes.md).

 

 



