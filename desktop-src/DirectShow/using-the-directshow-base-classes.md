---
description: utilisation des Classes de Base DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: utilisation des Classes de Base DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857409"
---
# <a name="using-the-directshow-base-classes"></a>utilisation des Classes de Base DirectShow

pour utiliser les classes de base dans DirectShow, vous devez générer et lier la bibliothèque de classes de base.

la bibliothèque de classes de base est fournie en tant qu’exemple sdk dans le kit de développement logiciel (sdk) de Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ). L’emplacement exact dépend de la version du kit de développement logiciel (SDK) que vous avez installée, mais le chemin d’accès relatif est le suivant :

*(Racine des exemples du kit de développement logiciel)* \\ DirectShow \\ BaseClasses

en-tête : Flux. h

Bibliothèque : l’exemple génère des versions commerciales et de débogage de la bibliothèque :

-   Version commerciale : Strmbase. lib
-   Version de débogage : Strmbasd. lib.

Pour plus d’informations sur la configuration de votre environnement de génération, consultez [configuration de l’environnement de génération](setting-up-the-build-environment.md).

## <a name="preprocessor-symbols"></a>Symboles du préprocesseur

lorsque vous incluez le fichier d’en-tête Flux. h, les symboles de préprocesseur suivants ont une signification particulière :

-   PERF : réservé. N’utilisez pas ce symbole de préprocesseur.
-   VFWROBUST : active la validation de pointeur dans Retail. Pour plus d’informations, consultez [macros de validation de pointeurs](pointer-validation-macros.md). Dans les versions Debug, il n’est pas nécessaire de définir VFWROBUST.

> [!Note]  
> dans Windows Vista et versions ultérieures, les macros de validation du pointeur sont vides.

 

 

 



