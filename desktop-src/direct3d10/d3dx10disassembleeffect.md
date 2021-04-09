---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DDisassemble. Cette fonction, qui Désassemble un effet compilé dans une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, est dépréciée.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: D3DX10DisassembleEffect, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953922"
---
# <a name="d3dx10disassembleeffect-function"></a>D3DX10DisassembleEffect fonction)

> [!Note]  
> Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

Cette fonction, qui Désassemble un effet compilé dans une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, est dépréciée. Utilisez plutôt [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pEffect* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

Pointeur vers l’interface d’effet (voir [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).

</dd> <dt>

*EnableColorCode* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Incluez des balises HTML dans la sortie pour coder en couleur le résultat.

</dd> <dt>

*ppDisassembly* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’une mémoire tampon (voir [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient l’effet désassemblé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
