---
title: Services de sérialisation
description: Microsoft RPC prend en charge deux méthodes d’encodage et de décodage des données, collectivement appelées sérialisation de données.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- Appel de procédure distante RPC, description, sérialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54e6daf4ace5ffb3ee5d22886a570ae1e9ab1ae834cfac12a91d234c331e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035529"
---
# <a name="serialization-services"></a>Services de sérialisation

Microsoft RPC prend en charge deux méthodes d’encodage et de décodage des données, collectivement appelées *sérialisation de données*. La sérialisation signifie que les données sont marshalées vers et démarshalées à partir des mémoires tampons que vous contrôlez. Cela diffère de l’utilisation traditionnelle de RPC, dans laquelle les stubs et la bibliothèque Runtime RPC disposent d’un contrôle total sur les mémoires tampons de marshaling et le processus est transparent. Vous pouvez utiliser la mémoire tampon pour le stockage sur un support permanent, le chiffrement, etc. Lorsque vous encodez des données, les stubs RPC marshalent les données dans une mémoire tampon et la transmettent à votre mémoire tampon. Lorsque vous décodez des données, vous fournissez une mémoire tampon de marshaling avec des données, et les données sont démarshalées de la mémoire tampon en mémoire. Vous pouvez sérialiser sur une base de procédure ou de type.

> [!Note]  
> Le terme « *picking* » est couramment utilisé parmi les développeurs pour décrire la sérialisation. en fait, les exemples de SDK Windows contiennent un répertoire appelé *pickle* qui conserve les exemples de programmes de sérialisation RPC.

 

La sérialisation utilise les mécanismes RPC pour le marshaling et le démarshaling des données à d’autres fins. Par exemple, au lieu d’utiliser plusieurs opérations d’e/s pour sérialiser un groupe d’objets dans un flux, une application peut optimiser les performances en sérialisant plusieurs objets de types différents dans une mémoire tampon, puis en écrivant l’intégralité de la mémoire tampon en une seule opération. Les fonctions qui manipulent des handles de sérialisation sont indépendantes du type de sérialisation que vous utilisez.

autre exemple, si vous avez besoin d’utiliser un mécanisme de transport réseau autre que RPC, tel que Microsoft Windows sockets (Winsock). Avec la sérialisation RPC, votre programme peut effectuer des appels à des fonctions qui marshalent vos données dans des mémoires tampons et transmettent ces données à l’aide de Winsock. Lorsque votre application reçoit des données, elle peut utiliser le mécanisme de sérialisation RPC pour démarshaler les données des mémoires tampons remplies par les routines Winsock. Cela vous offre de nombreux avantages des applications de style RPC et, en même temps, vous permet d’utiliser des mécanismes de transport non-RPC.

Vous pouvez également utiliser la sérialisation à des fins non liées aux communications réseau. Par exemple, une fois que vous utilisez les fonctions d’encodage RPC pour marshaler des données dans une mémoire tampon, vous pouvez les stocker dans un fichier pour une utilisation par une autre application. Vous pouvez également la chiffrer. Vous pouvez même l’utiliser pour stocker une représentation indépendante du matériel et du système d’exploitation des données dans une base de données.

Les rubriques suivantes présentent une discussion sur les services de sérialisation pris en charge par Microsoft RPC :

-   [Utilisation des services de sérialisation](using-serialization-services.md)
-   [Sérialisation de procédure](procedure-serialization.md)
-   [Sérialisation de type](type-serialization.md)
-   [Handles de sérialisation](serialization-handles.md)

 

 




