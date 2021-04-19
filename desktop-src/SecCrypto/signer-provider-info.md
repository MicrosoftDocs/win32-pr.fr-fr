---
description: Spécifie les informations du fournisseur de services de chiffrement (CSP) et de la clé privée utilisées pour créer une signature numérique.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Structure SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521109"
---
# <a name="signer_provider_info-structure"></a>Structure d' \_ informations du fournisseur de signataires \_

La structure d' **\_ \_ informations du fournisseur de signataires** spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de clé privée utilisés pour créer une signature numérique.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**pwszProviderName**
</dt> <dd>

Nom du fournisseur de services de chiffrement utilisé pour créer la signature numérique. Si la valeur de ce membre est **null**, le fournisseur par défaut est utilisé.

</dd> <dt>

**dwProviderType**
</dt> <dd>

Type du fournisseur de services de chiffrement spécifié par le membre **pwszProviderName** .

</dd> <dt>

**dwKeySpec**
</dt> <dd>

Spécification de la clé. Si ce membre a la valeur zéro, la spécification de clé dans le membre **pwszPvkFileName** ou **pwszKeyContainer** est utilisée. S’il existe plus d’une spécification de clé dans le membre **pwszKeyContainer** , **at \_ signature** est utilisé. En cas d’échec, à l’utilisation **de \_ KeyExchange** .

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Spécifie le type d’informations de clé privée. Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                               | Signification                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**Pvk \_ TAPEZ \_ le \_ nom de fichier**</dt> <dt>1 (0x1)</dt> </dl>         | Les informations de la clé privée sont un nom de fichier.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**Pvk \_ TAPEZ \_ keycontainer**</dt> <dt>2 (0X2)</dt> </dl> | Les informations de la clé privée sont un conteneur de clé.<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

Nom du fichier qui contient les informations sur la clé privée.

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

Nom du conteneur de clé qui contient les informations sur la clé privée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
