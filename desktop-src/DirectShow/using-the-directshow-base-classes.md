---
description: Utilisation des classes de base DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Utilisation des classes de base DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203621"
---
# <a name="using-the-directshow-base-classes"></a>Utilisation des classes de base DirectShow

Pour utiliser les classes de base dans DirectShow, vous devez générer et lier la bibliothèque de classes de base.

La bibliothèque de classes de base est fournie en tant qu’exemple SDK dans le kit de développement logiciel (SDK) Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ). L’emplacement exact dépend de la version du kit de développement logiciel (SDK) que vous avez installée, mais le chemin d’accès relatif est le suivant :

*(Racine des exemples du kit de développement logiciel)* \\ \\BaseClasses DirectShow

En-tête : streams. h

Bibliothèque : l’exemple génère des versions commerciales et de débogage de la bibliothèque :

-   Version commerciale : Strmbase. lib
-   Version de débogage : Strmbasd. lib.

Pour plus d’informations sur la configuration de votre environnement de génération, consultez [configuration de l’environnement de génération](setting-up-the-build-environment.md).

## <a name="preprocessor-symbols"></a>Symboles du préprocesseur

Lorsque vous incluez le fichier d’en-tête streams. h, les symboles de préprocesseur suivants ont une signification particulière :

-   PERF : réservé. N’utilisez pas ce symbole de préprocesseur.
-   VFWROBUST : active la validation de pointeur dans Retail. Pour plus d’informations, consultez [macros de validation de pointeurs](pointer-validation-macros.md). Dans les versions Debug, il n’est pas nécessaire de définir VFWROBUST.

> [!Note]  
> Dans Windows Vista et versions ultérieures, les macros de validation du pointeur sont vides.

 

 

 



