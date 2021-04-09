---
description: L’extensibilité est obtenue en fournissant l’utilisation de nouveaux identificateurs d’objet (OID), de nouveaux types d’encodage et de nouvelles dll.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Vue d’ensemble des OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866966"
---
# <a name="oid-overview"></a><span data-ttu-id="2a5b6-103">Vue d’ensemble des OID</span><span class="sxs-lookup"><span data-stu-id="2a5b6-103">OID Overview</span></span>

<span data-ttu-id="2a5b6-104">L’extensibilité est obtenue en fournissant l’utilisation de nouveaux [*identificateurs d’objet*](../secgloss/o-gly.md) (OID), de nouveaux types d’encodage et de nouvelles dll.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="2a5b6-105">Les OID CryptoAPI peuvent prendre l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a5b6-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="2a5b6-106">Chaîne numérique telle que « 1.2.3.500.88 »</span><span class="sxs-lookup"><span data-stu-id="2a5b6-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="2a5b6-107">Chaîne alphanumérique telle que *MyFunction*</span><span class="sxs-lookup"><span data-stu-id="2a5b6-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="2a5b6-108">Constante dont la valeur est inférieure ou égale à 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="2a5b6-109">Ces constantes sont souvent associées à un nom via l’utilisation d’une instruction de **\# définition** dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="2a5b6-110">Les fonctions extensibles acceptent les arguments de type OID et Encoding.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="2a5b6-111">Ces fonctions recherchent dans le registre système une DLL associée à l’OID et les arguments de type d’encodage passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="2a5b6-112">Si une DLL pour l’OID, la combinaison du type d’encodage est trouvée, la DLL est chargée et sa fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="2a5b6-113">L’illustration suivante montre ce processus pour la fonction [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :</span><span class="sxs-lookup"><span data-stu-id="2a5b6-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![Workflow d’OID](images/oidflow.png)

<span data-ttu-id="2a5b6-115">Cela permet d’étendre les fonctionnalités de l’CryptoAPI en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="2a5b6-116">L’utilisation de cette méthodologie complique le développement de la nouvelle fonctionnalité pour écrire tout le code nécessaire pour cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="2a5b6-117">Pour encoder une nouvelle structure de données, par exemple, la fonction dans la DLL doit exécuter l’intégralité du processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="2a5b6-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
