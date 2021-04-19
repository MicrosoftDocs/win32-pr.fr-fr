---
description: Spécifie un fichier à signer.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Structure SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524444"
---
# <a name="signer_file_info-structure"></a>Structure d' \_ informations du fichier signataire \_

La structure d' **\_ \_ informations du fichier de signataire** spécifie un fichier à signer.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**pwszFileName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du fichier à signer.

</dd> <dt>

**hFile**
</dt> <dd>

Handle ouvert du fichier spécifié par le membre **pwszFileName** . Si ce membre contient un handle valide, ce handle est utilisé pour accéder au fichier. Ce membre peut avoir la valeur **null**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**informations d' \_ objet du signataire \_**](signer-subject-info.md)
</dt> </dl>

 

 




