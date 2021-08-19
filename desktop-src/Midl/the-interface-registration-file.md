---
title: Fichier d’inscription de l’interface
description: Le fichier d’inscription de l’interface collecte des informations qui facilitent l’inscription des interfaces COM empaquetées dans un fichier DLL ou EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- MIDL du fichier d’inscription de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a5541a5e60b1903364236f86dcf1845a5e1ac153fc91b47bacf9f553a9a109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806177"
---
# <a name="the-interface-registration-file"></a>Fichier d’inscription de l’interface

Le fichier d’inscription de l’interface collecte des informations qui facilitent l’inscription des interfaces COM empaquetées dans un fichier DLL ou EXE. Le fichier d’inscription de l’interface est différent des autres fichiers générés, car il peut recueillir des informations à partir de la compilation de plusieurs fichiers IDL différents. Chaque compilateur MIDL exécuté pour les interfaces COM recherche d’abord un fichier dlldata. c existant, et si le fichier est introuvable, un nouveau fichier dlldata. c est créé. Si un fichier dlldata. c est trouvé, des informations sur l’IDL actuel sont ajoutées (si absentes) ou remplacées.

Le fichier d’inscription de l’interface est généré ou mis à jour en toute sécurité dans un environnement multiprocesseur, car les compilations MIDL parallèles ne peuvent pas écrire dans le fichier en même temps. Étant donné que tout fichier dlldata. c peut être marqué comme étant en lecture seule par l’environnement de génération ou l’utilisateur, le compilateur MIDL implémente une approche du délai d’attente pour attendre un fichier qu’il ne peut pas ouvrir et émet un message d’erreur approprié si le délai d’attente expire.

Le nom par défaut du fichier d’inscription de l’interface généré à partir d’un fichier d’entrée est dlldata. c. Le commutateur du compilateur MIDL [**/dlldata**](-dlldata.md) peut être utilisé pour remplacer le nom par défaut du fichier. Le remplacement du nom par défaut du fichier d’inscription de l’interface est particulièrement utile lorsque certains fichiers IDL empaquetés dans un fichier binaire commun résident dans des répertoires différents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération et inscription d’une DLL proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 