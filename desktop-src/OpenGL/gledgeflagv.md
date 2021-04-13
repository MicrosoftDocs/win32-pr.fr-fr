---
title: fonction glEdgeFlagv (GL. h)
description: Signale les bords comme une limite ou une non-limite. | fonction glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- glEdgeFlagv fonction OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322245"
---
# <a name="gledgeflagv-function"></a>glEdgeFlagv fonction)

Signale les bords comme une limite ou une non-limite.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*flag* 
</dt> <dd>

Spécifie un pointeur vers un tableau qui contient un seul élément booléen, qui remplace la valeur de l’indicateur de bord actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque vertex d’un polygone, d’un triangle distinct ou d’un quadrilatère distinct spécifié entre une paire [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) est marqué comme le début d’une limite ou d’un bord non limité. Si l’indicateur de bord actuel a la **valeur true** lorsque le vertex est spécifié, le vertex est marqué comme le début d’un bord de limite. Si l’indicateur de bord actuel a la **valeur false**, le vertex est marqué comme le début d’un bord non lié. La fonction **glEdgeFlagv** affecte la **valeur true** à l’indicateur Edge si l’indicateur est différent de zéro ; sinon, **false** .

Les vertex des triangles connectés et des quadrilatères connectés sont toujours marqués comme limites, quelle que soit la valeur de l’indicateur de bord.

Les indicateurs de limite et de périphérie non frontière sur les vertex ne sont significatifs que si le \_ mode de polygone GL \_ est défini sur le point GL ou sur la \_ \_ ligne GL. Consultez [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Initialement, le bit de l’indicateur Edge a la **valeur true**.

L’indicateur de périphérie actuel peut être mis à jour à tout moment. En particulier, **glEdgeFlagv** peut être appelé entre un appel à [**glBegin**](/windows/desktop/OpenGL/glbegin) et l’appel correspondant à [**glEnd**](/windows/desktop/OpenGL/glend).

Les fonctions suivantes récupèrent les informations relatives à **glEdgeFlagv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l' \_ indicateur de périphérie de l’argument GL \_

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

