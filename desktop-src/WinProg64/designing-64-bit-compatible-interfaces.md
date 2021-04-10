---
title: Conception d’interfaces compatibles 64 bits
description: Des problèmes de compatibilité descendante se produisent lorsque vous ajoutez de nouveaux types de données ou méthodes à une interface, modifiez les anciens types de données ou utilisez des types de données de manière inappropriée.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- compatibilité descendante avec la programmation Windows 64 bits
- interfaces compatibles 64 bits programmation Windows 64 bits
- Guide de programmation Windows 64 bits, programmation Windows 64 bits, compatibilité
- compatibilité avec la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309946"
---
# <a name="designing-64-bit-compatible-interfaces"></a>Conception d’interfaces compatibles 64 bits

Le portage à partir de Windows 32 bits vers Windows 64 bits ne doit pas, en soi, créer des problèmes pour les applications distribuées, qu’ils utilisent des appels de procédure distante (RPC) directement ou via DCOM. Le modèle de programmation RPC spécifie des tailles de données bien définies et des types d’entiers de la même taille à chaque extrémité de la connexion. En outre, dans le modèle de données abstraites LLP64 développé pour Windows 64 bits, seuls les pointeurs sont étendus à 64 bits : tous les autres types de données Integer restent 32 bits. Étant donné que les pointeurs sont locaux de chaque côté de la connexion client/serveur et sont généralement transmis en tant que marqueurs **null** ou non **null** , le moteur de marshaling peut gérer des tailles de pointeur différentes à la fin d’une connexion de manière transparente.

Toutefois, des problèmes de compatibilité descendante se produisent lorsque vous ajoutez de nouveaux types de données ou de nouvelles méthodes à une interface, modifiez des types de données anciens ou utilisez des types de données de manière inappropriée. Les rubriques suivantes expliquent comment éviter ces situations (lorsque cela est possible) et comment concevoir des solutions de contournement robustes lorsqu’il n’est pas possible de les éviter.

## <a name="in-this-section"></a>Dans cette section

-   [Modification d’une interface existante](changing-an-existing-interface.md)
-   [Éviter le masquage des informations](avoiding-information-hiding.md)
-   [Éviter le polymorphisme](avoiding-polymorphism.md)
-   [Utilisation de nouveaux types de données dans votre fichier IDL](using-new-data-types-in-your-idl-file.md)
-   [Préparation de votre application pour Windows 64 bits](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>Sections connexes

Si vous n’êtes pas déjà familiarisé avec les nouveaux types de données, l’environnement de travail et les modifications d’API pour Windows 64 bits, consultez [préparation pour windows 64 bits](getting-ready-for-64-bit-windows.md).

 

 




