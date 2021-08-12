---
description: CABINETDLLVERSIONINFO contient les informations de version pour Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: CABINETDLLVERSIONINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9276a03d28bdfeee2b97b44e180bf190cbf20fc40ec58d0aafb44962a6e8fa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667982"
---
# <a name="cabinetdllversioninfo-structure"></a>CABINETDLLVERSIONINFO, structure

\[Cette structure contient des informations requises uniquement lors de l’utilisation de la fonction **DllGetVersion** , ce qui n’est pas pris en charge. Cette documentation est fournie à titre d’information uniquement.\]

**CABINETDLLVERSIONINFO** contient les informations de version pour Cabinet.dll.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbStruct**
</dt> <dd>

Taille de cette structure, en octets.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Réservé.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Réservé.

</dd> <dt>

**dwFileVersionMS**
</dt> <dd>

Contient les bits les plus significatifs des informations sur la version. Bits 0-15 contient la version mineure et bits 16-31 contient la version principale.

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

Contient les bits les moins significatifs des informations de version. Bits 0-15 contiennent le numéro de révision, et les bits 16-31 contiennent le numéro de Build.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



