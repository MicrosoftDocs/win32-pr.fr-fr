---
description: La structure EXPERTFRAMEDESCRIPTOR contient des informations sur un frame. Lorsque l’expert appelle la fonction ExpertGetFrame avec succès, Moniteur réseau transmet la structure EXPERTFRAMEDESCRIPTOR à l’expert.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: EXPERTFRAMEDESCRIPTOR, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110377"
---
# <a name="expertframedescriptor-structure"></a>EXPERTFRAMEDESCRIPTOR, structure

La structure **EXPERTFRAMEDESCRIPTOR** contient des informations sur un frame. Lorsque l’expert appelle la fonction [**ExpertGetFrame**](expertgetframe.md) avec succès, moniteur réseau transmet la structure **EXPERTFRAMEDESCRIPTOR** à l’expert.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>Membres

<dl> <dt>

**FrameNumber**
</dt> <dd>

Numéro d’un cadre spécifié.

</dd> <dt>

**hFrame**
</dt> <dd>

Handle vers un frame.

</dd> <dt>

**pFrame**
</dt> <dd>

Pointeur vers un frame brut.

</dd> <dt>

**lpRecognizeDataTable**
</dt> <dd>

Table qui indique où chaque analyseur identifie le début des données.

</dd> <dt>

**lpPropertyTable**
</dt> <dd>

Table de propriétés de frame identifiée par l’analyseur.

</dd> </dl>

## <a name="remarks"></a>Notes

Si l’expert spécifie des \_ propriétés d’attachement de balises \_ lors de l’appel de [**ExpertGetFrame**](expertgetframe.md), le membre **szPropertyText** dans chaque structure [**PROPERTYINST**](propertyinst.md) a la **valeur null**.

Si l’expert ne spécifie pas \_ les \_ propriétés d’attachement des indicateurs lors de l’appel de la fonction [**ExpertGetFrame**](expertgetframe.md) , le membre **lpPropertyTable** est **null** au retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




