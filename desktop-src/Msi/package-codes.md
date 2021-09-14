---
description: le code du package est un GUID identifiant un package de Windows Installer particulier.
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: Codes de package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218825"
---
# <a name="package-codes"></a>Codes de package

le code du package est un GUID identifiant un [*package*](p-gly.md)de Windows Installer particulier. Le code du package associe un fichier .msi à une application ou un produit et peut également être utilisé pour la vérification des sources. Les codes de produit et de package ne sont pas interchangeables. Pour plus d’informations, consultez [Product Codes](product-codes.md).

Les fichiers de .msi non identiques ne doivent pas avoir le même code de package. Il est important de modifier le code du package, car il s’agit de l’identificateur principal utilisé par le programme d’installation pour rechercher et valider le package approprié pour une installation donnée. Si un package est modifié sans modifier le code du package, le programme d’installation peut ne pas utiliser le package le plus récent si les deux sont toujours accessibles au programme d’installation.

Le code du package est stocké dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) du flux d’informations de [synthèse](summary-information-stream.md). Notez que les lettres du code du produit et des GUID du code du package doivent être en majuscules. Les utilitaires tels que GUIDGEN génèrent des GUID contenant des minuscules. Les minuscules dans ces GUID doivent être remplacées par des majuscules à utiliser comme code de produit ou code de package.

Bien qu’il soit courant d’expédier une application qui possède le même code de package et le même code de produit, les deux valeurs peuvent divergent lorsque l’application est mise à jour. Par exemple, l’inclusion d’un nouveau fichier avec l’application nécessite la mise à jour de la base de données d’installation pour installer le fichier. Si les modifications sont mineures, un développeur peut choisir de ne pas modifier le code du produit. Toutefois, un fichier de .msi différent est nécessaire pour installer le nouveau fichier et le code du package doit donc être incrémenté. À l’inverse, un seul package peut être utilisé pour installer plusieurs produits. Par exemple, l’installation d’un package sans transformation de langage peut installer la version anglaise de l’application et l’installation du même package avec une transformation de langue peut installer la version française. La transformation est distincte du fichier .msi qui détermine le code du package. Les versions anglaise et française peuvent avoir des codes de produit différents et le même code de package, car ils sont tous deux installés avec le même fichier .msi.

 

 



