---
description: L’extensibilité est obtenue en fournissant l’utilisation de nouveaux identificateurs d’objet (OID), de nouveaux types d’encodage et de nouvelles dll.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Vue d’ensemble des OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123106"
---
# <a name="oid-overview"></a>Vue d’ensemble des OID

L’extensibilité est obtenue en fournissant l’utilisation de nouveaux [*identificateurs d’objet*](../secgloss/o-gly.md) (OID), de nouveaux types d’encodage et de nouvelles dll.

Les OID CryptoAPI peuvent prendre l’une des formes suivantes :

-   Chaîne numérique telle que « 1.2.3.500.88 »
-   Chaîne alphanumérique telle que *MyFunction*
-   Constante dont la valeur est inférieure ou égale à 0xFFFF. Ces constantes sont souvent associées à un nom via l’utilisation d’une instruction de **\# définition** dans un fichier d’en-tête.

Les fonctions extensibles acceptent les arguments de type OID et Encoding. Ces fonctions recherchent dans le registre système une DLL associée à l’OID et les arguments de type d’encodage passés à la fonction. Si une DLL pour l’OID, la combinaison du type d’encodage est trouvée, la DLL est chargée et sa fonction est appelée. L’illustration suivante montre ce processus pour la fonction [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :

![Workflow d’OID](images/oidflow.png)

Cela permet d’étendre les fonctionnalités de l’CryptoAPI en fonction des besoins. L’utilisation de cette méthodologie complique le développement de la nouvelle fonctionnalité pour écrire tout le code nécessaire pour cette fonctionnalité. Pour encoder une nouvelle structure de données, par exemple, la fonction dans la DLL doit exécuter l’intégralité du processus d’encodage.

 

 
