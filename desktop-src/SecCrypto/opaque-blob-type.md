---
description: Les objets BLOB opaques, également appelés OPAQUEKEYBLOBs, sont utilisés pour stocker les clés de session dans un format spécifique au fournisseur, tel que Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Type d’objet BLOB opaque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393768"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="03e55-103">Type d’objet BLOB opaque</span><span class="sxs-lookup"><span data-stu-id="03e55-103">Opaque BLOB Type</span></span>

<span data-ttu-id="03e55-104">Les [*objets BLOB opaques*](../secgloss/o-gly.md), également appelés OPAQUEKEYBLOBs, sont utilisés pour stocker les [*clés de session*](../secgloss/s-gly.md) dans un format spécifique au fournisseur, tel que [*Schannel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="03e55-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="03e55-105">Ils contiennent le matériel de clé de base et toutes les informations d' [*État*](../secgloss/s-gly.md) actuelles.</span><span class="sxs-lookup"><span data-stu-id="03e55-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="03e55-106">Cela comprend des informations telles que la [*valeur Salt*](../secgloss/s-gly.md), le [*vecteur d’initialisation*](../secgloss/i-gly.md)et la table clé.</span><span class="sxs-lookup"><span data-stu-id="03e55-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="03e55-107">Le format des objets BLOB opaques n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="03e55-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="03e55-108">Chaque fournisseur de services de chiffrement détermine son propre format d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="03e55-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="03e55-109">Étant donné qu’une clé est exportée dans un objet BLOB opaque dans un format spécifique au CSP, elle ne peut être importée que dans le CSP à partir duquel elle a été exportée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="03e55-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="03e55-110">Lorsque deux processus sont impliqués, chaque [*processus*](../secgloss/p-gly.md) appelle [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) indépendamment.</span><span class="sxs-lookup"><span data-stu-id="03e55-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="03e55-111">Chaque processus obtient un handle vers un conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="03e55-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="03e55-112">Il est possible que les deux processus aient des handles vers le même conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="03e55-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="03e55-113">Un processus crée les clés et les exporte dans des objets BLOB opaques, puis transmet les objets BLOB au deuxième processus.</span><span class="sxs-lookup"><span data-stu-id="03e55-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="03e55-114">Le deuxième processus importe les clés de l’objet BLOB dans son [*conteneur de clé*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="03e55-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="03e55-115">Si un fournisseur de services de chiffrement de matériel ne prend pas en charge l’exportation des clés, l’objet BLOB peut uniquement contenir l’index d’un registre de clés, ou un nom similaire.</span><span class="sxs-lookup"><span data-stu-id="03e55-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="03e55-116">Dans ce cas, le reste de la procédure est ignoré.</span><span class="sxs-lookup"><span data-stu-id="03e55-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
