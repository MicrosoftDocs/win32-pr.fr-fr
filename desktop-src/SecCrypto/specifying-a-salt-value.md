---
description: Le fournisseur de base et le fournisseur étendu peuvent spécifier la valeur et la longueur de la valeur Salt à utiliser. Le fournisseur de base définit une valeur Salt à l’aide de la \_ valeur de paramètre Salt de KP. Le fournisseur de base définit toujours onze octets de valeur salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Spécification d’une valeur Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d80ca64bc69cbcf0ed98d72b5b061616fc3cf641f3970d1533b094ef5687f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897944"
---
# <a name="specifying-a-salt-value"></a>Spécification d’une valeur Salt

Le fournisseur de base et le fournisseur étendu peuvent spécifier la valeur et la longueur de la [*valeur Salt*](../secgloss/s-gly.md) à utiliser. Le fournisseur de base définit une valeur Salt à l’aide de la \_ valeur de paramètre Salt de KP. Le fournisseur de base définit toujours onze octets de valeur salt.

Le fournisseur amélioré définit la valeur Salt en appelant [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) avec la valeur de paramètre de KP \_ Salt \_ ex spécifiée et avec le paramètre *pbData* qui pointe vers une structure [**\_ \_ BLOB d’entiers de chiffre**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) qui contient le Salt.

> [!Note]  
> La longueur totale d’une [*clé symétrique*](../secgloss/s-gly.md) de fournisseur amélioré et de sa valeur Salt ne peut pas être supérieure à 128 bits.

 

\_Le Salt de KP continue à être fourni pour la compatibilité descendante avec le fournisseur de base. Les applications plus récentes doivent utiliser la valeur de paramètre de KP \_ sel \_ ex.

L’exemple suivant définit une valeur salt.


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



 

 
