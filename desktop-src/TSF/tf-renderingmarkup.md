---
title: Structure TF_RENDERINGMARKUP
description: La structure de la \_ structure RENDERINGMARKUP TF contient une plage et les informations d’attribut d’affichage.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP structure Text Services Framework
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106512071"
---
# <a name="tf_renderingmarkup-structure"></a>\_Structure RENDERINGMARKUP TF

La structure de la structure [**\_ RENDERINGMARKUP TF**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contient une plage et les informations d’attribut d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Membres

<dl> <dt>

**pRange**
</dt> <dd>

Pointeur vers une interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .

</dd> <dt>

**tfDisplayAttr**
</dt> <dd>

Affichez les informations d’attribut.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas actuellement dans les fichiers d’en-tête publics. Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).

 

 




