---
description: Le fournisseur de base et le fournisseur étendu peuvent spécifier la valeur et la longueur de la valeur Salt à utiliser. Le fournisseur de base définit une valeur Salt à l’aide de la \_ valeur de paramètre Salt de KP. Le fournisseur de base définit toujours onze octets de valeur salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Spécification d’une valeur Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542992"
---
# <a name="specifying-a-salt-value"></a><span data-ttu-id="02a2a-105">Spécification d’une valeur Salt</span><span class="sxs-lookup"><span data-stu-id="02a2a-105">Specifying a Salt Value</span></span>

<span data-ttu-id="02a2a-106">Le fournisseur de base et le fournisseur étendu peuvent spécifier la valeur et la longueur de la [*valeur Salt*](../secgloss/s-gly.md) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="02a2a-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="02a2a-107">Le fournisseur de base définit une valeur Salt à l’aide de la \_ valeur de paramètre Salt de KP.</span><span class="sxs-lookup"><span data-stu-id="02a2a-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="02a2a-108">Le fournisseur de base définit toujours onze octets de valeur salt.</span><span class="sxs-lookup"><span data-stu-id="02a2a-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="02a2a-109">Le fournisseur amélioré définit la valeur Salt en appelant [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) avec la valeur de paramètre de KP \_ Salt \_ ex spécifiée et avec le paramètre *pbData* qui pointe vers une structure [**\_ \_ BLOB d’entiers de chiffre**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) qui contient le Salt.</span><span class="sxs-lookup"><span data-stu-id="02a2a-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="02a2a-110">La longueur totale d’une [*clé symétrique*](../secgloss/s-gly.md) de fournisseur amélioré et de sa valeur Salt ne peut pas être supérieure à 128 bits.</span><span class="sxs-lookup"><span data-stu-id="02a2a-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="02a2a-111">\_Le Salt de KP continue à être fourni pour la compatibilité descendante avec le fournisseur de base.</span><span class="sxs-lookup"><span data-stu-id="02a2a-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="02a2a-112">Les applications plus récentes doivent utiliser la valeur de paramètre de KP \_ sel \_ ex.</span><span class="sxs-lookup"><span data-stu-id="02a2a-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="02a2a-113">L’exemple suivant définit une valeur salt.</span><span class="sxs-lookup"><span data-stu-id="02a2a-113">The following example sets a salt value.</span></span>


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
