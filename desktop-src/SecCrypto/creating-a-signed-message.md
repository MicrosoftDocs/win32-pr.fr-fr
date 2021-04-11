---
description: Décrit les tâches qui doivent être effectuées pour créer un message signé.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Création d’un message signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203553"
---
# <a name="creating-a-signed-message"></a>Création d’un message signé

L’illustration suivante représente les tâches qui doivent être accomplies pour créer un message signé. Les étapes sont répertoriées à la suite de l’illustration.

![signature d’un message](images/signdmsg.png)

**Pour créer un message signé**

1.  Créez les données (si nécessaire) et recevez un pointeur vers celle-ci.
2.  Ouvrez un [*magasin de certificats*](../secgloss/c-gly.md) qui contient le certificat du signataire.
3.  Obtenir la [*clé privée*](../secgloss/p-gly.md) du certificat. Une propriété doit être définie sur le certificat avant de l’utiliser pour lier un certificat à un [*CSP*](../secgloss/c-gly.md)particulier, et, dans ce CSP, à une clé privée particulière. Cela doit être défini une seule fois.
4.  Choisissez un algorithme de hachage pour l’opération Digest. Nous vous recommandons de sélectionner l’algorithme de hachage à partir d’un emplacement configurable qui peut être mis à jour par la suite sans qu’il soit nécessaire de modifier le code.
5.  Envoyer les données par le biais de la fonction de hachage à l’aide de l’algorithme de hachage, créant ainsi un [*hachage*](../secgloss/h-gly.md) (Digest) des données.
6.  À l’aide de la [*clé privée*](../secgloss/p-gly.md) obtenue par le biais de la propriété sur le certificat, chiffrez le condensé et créez la signature.
7.  Incluez ce qui suit dans le message signé :

    -   Données signées
    -   Algorithme de hachage
    -   La signature
    -   Identificateur du signataire (émetteur et numéro de série du certificat)
    -   Le certificat du signataire (facultatif)

Pour obtenir une procédure détaillée et un exemple, consultez [procédure de signature des données](procedure-for-signing-data.md) et [exemple de programme C : signature d’un message et vérification d’une signature de message](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
