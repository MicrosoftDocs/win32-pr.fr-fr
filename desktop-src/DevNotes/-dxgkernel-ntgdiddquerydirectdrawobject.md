---
description: Interroge une représentation en mode noyau précédemment créée d’un objet Microsoft DirectDraw pour ses fonctionnalités.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: NtGdiDdQueryDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103819"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>NtGdiDdQueryDirectDrawObject fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Interroge une représentation en mode noyau précédemment créée d’un objet Microsoft DirectDraw pour ses fonctionnalités.

## <a name="syntax"></a>Syntaxe


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDrawLocal* \[ dans\]
</dt> <dd>

Handle vers l’appareil DirectDraw en mode noyau précédemment créé.

</dd> <dt>

*pHalInfo* \[ à\]
</dt> <dd>

Pointeur vers une [**structure \_ HALINFO DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) qui sera remplie avec les fonctionnalités de l’appareil. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Pointeur vers une mémoire tampon fournie par l’appelant qui stocke des indicateurs de rappel signalés par un pilote. La mémoire tampon doit être d’une taille de 3 \* sizeof (DWORD) et stocke les indicateurs de rappel dans l’ordre suivant : pCallBackFlags \[ 0 \] pour les indicateurs dans les [**\_ rappels DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), PCallBackFlags \[ 1 \] pour les indicateurs dans [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)et pCallBackFlags \[ 2 \] pour les indicateurs dans [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*puD3dCallbacks* \[ à\]
</dt> <dd>

Pointeur vers un tableau de pointeurs de rappel Direct3D. La table est remplie avec des pointeurs vers des fonctions dans Gdi32.dll qui imitent un pilote d’affichage Direct3D. Cette table de rappel est identique à la \_ structure D3DHAL D3DCALLBACKS décrite dans la documentation du DDK.

</dd> <dt>

*puD3dDriverData* \[ à\]
</dt> <dd>

Pointeur vers [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) Data, comme décrit dans la documentation du DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ à\]
</dt> <dd>

Pointeur vers un tableau de pointeurs de rappel. La table est remplie avec des pointeurs vers des fonctions dans Gdi32.dll qui imitent un pilote d’affichage Direct3D. Cette table de rappel est identique à la \_ structure DDHAL DDEXEBUFCALLBACKS, qui est mappée à la structure [**DD de \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) décrite dans la documentation du DDK, sauf que les membres XxxD3DBuffer dans **DD \_ D3DBUFCALLBACKS** sont remplacés par XxxExecuteBuffer dans DDHAL \_ DDEXEBUFCALLBACKS.

</dd> <dt>

*puD3dTextureFormats* \[ à\]
</dt> <dd>

Pointeur vers un tableau de structures [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) qui définissent le jeu de formats de texture autorisés.

</dd> <dt>

*puNumHeaps* \[ à\]
</dt> <dd>

Pointeur vers le membre **dwNumHeaps** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**. Le membre **dwNumHeaps** spécifie le nombre de segments de mémoire dans *puvmList*. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*puvmList* \[ à\]
</dt> <dd>

Pointeur vers une liste de descripteurs de tas de mémoire vidéo. Peut avoir la **valeur null**. Ce paramètre n’est pas utilisé, car la gestion de la mémoire vidéo est gérée entièrement en mode noyau.

</dd> <dt>

*puNumFourCC* \[ à\]
</dt> <dd>

Pointeur vers le membre **puNumFourCCCodes** de [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. Le membre **puNumFourCCCodes** spécifie le nombre de codes [à quatre caractères (FourCC)](../directshow/fourcc-codes.md) pris en charge par le pilote. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*puFourCC* \[ à\]
</dt> <dd>

Pointeur désignant une liste de formats de surface de [codes à quatre caractères (FourCC)](../directshow/fourcc-codes.md) pris en charge. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Un appel à cette fonction est conçu pour être effectué dans un processus en deux étapes. Dans la première étape, *puFourCC*, *puvmList* et *PuD3dTextureFormats* doivent avoir la **valeur null**, et [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) remplira le [**\_ HALINFO DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **DD \_ HALINFO**.**vmiData**. **dwNumHeaps** et [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** avec le nombre d’entrées qui doivent être retournées. Dans le deuxième appel, l’appelant doit allouer des tableaux de la taille indiquée et passer ces pointeurs au lieu de valeurs **null** dans les paramètres *puFourCC*, *puvmList* et *puD3dTextureFormats* . Les tableaux sont ensuite remplis avec les données appropriées.

Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques. Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des clients de bas niveau](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
