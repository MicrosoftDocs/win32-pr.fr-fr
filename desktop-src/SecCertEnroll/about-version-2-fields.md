---
description: Un certificat X.509 version 2 contient les champs de base définis dans la version 1, ainsi que les champs supplémentaires suivants.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Champs de la version 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201211"
---
# <a name="version-2-fields"></a><span data-ttu-id="44209-103">Champs de la version 2</span><span class="sxs-lookup"><span data-stu-id="44209-103">Version 2 Fields</span></span>

<span data-ttu-id="44209-104">Un certificat X.509 version 2 contient les champs de base définis dans la version 1, ainsi que les champs supplémentaires suivants.</span><span class="sxs-lookup"><span data-stu-id="44209-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="44209-105">Identificateur unique de l’émetteur</span><span class="sxs-lookup"><span data-stu-id="44209-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="44209-106">Contient une valeur unique pouvant être utilisée pour rendre le nom X.500 de l’autorité de certification non ambigu lorsqu’il est réutilisé par différentes entités au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="44209-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="44209-107">Identificateur unique du sujet</span><span class="sxs-lookup"><span data-stu-id="44209-107">Subject Unique Identifier</span></span>

<span data-ttu-id="44209-108">Contient une valeur unique pouvant être utilisée pour rendre le nom X.500 du sujet du certificat non ambigu lorsqu’il est réutilisé par différentes entités au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="44209-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="44209-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44209-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44209-110">Champs de base</span><span class="sxs-lookup"><span data-stu-id="44209-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="44209-111">Extensions de la version 3</span><span class="sxs-lookup"><span data-stu-id="44209-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="44209-112">Certificats de clé publique X. 509</span><span class="sxs-lookup"><span data-stu-id="44209-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



