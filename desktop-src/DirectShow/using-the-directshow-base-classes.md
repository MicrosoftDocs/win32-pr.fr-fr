---
description: utilisation des Classes de Base DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: utilisation des Classes de Base DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a0c8252022cf822e88ef7682b5dea4e53870b2a5aa21bd6a90fe87a15faa4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119298769"
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

 

 

 



