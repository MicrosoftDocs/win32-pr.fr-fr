---
title: Structure ORPC_DBG_BUFFER
description: La \_ structure de \_ mémoire tampon dbg ORPC est le format de mémoire tampon utilisé pour marshaler les données RPC vers les méthodes de l’interface IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- Structure COM ORPC_DBG_BUFFER
- Pointeur de structure PORPC_DBG_BUFFER COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb1f83cfcbe673cd2d5701e57ae1e94d4e04b59b845cd9ec7b617077da24bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310255"
---
# <a name="orpc_dbg_buffer-structure"></a>ORPC \_ , \_ structure de mémoire tampon dbg

La structure de **\_ \_ mémoire tampon dbg ORPC** est le format de mémoire tampon utilisé pour marshaler les données RPC vers les méthodes de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a>Membres

<dl> <dt>

**alwaysOrSometimes**
</dt> <dd>

Valeur qui contrôle la génération du débogueur. **alwaysOrSometimes** peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ Débogage \_ toujours**</dt> <dt>0x00000000</dt> </dl>                              | Si cette valeur est définie, COM déclenche toujours la notification du client ou du serveur sur le récepteur.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ Déboguer \_ si le \_ raccordement est \_ activé**</dt> <dt>0x00000001</dt> </dl> | Si cette option est définie, COM déclenche uniquement la notification du client ou du serveur sur le récepteur si le débogage COM a été activé en appelant [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) dans ce processus avec la valeur **true** affectée à **fTrace** . <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

Numéro de version principale de la spécification de format de données.

</dd> <dt>

**verMinor**
</dt> <dd>

Numéro de version mineure de la spécification de format de données.

</dd> <dt>

**cbRemaining**
</dt> <dd>

Nombre d’octets, inclus de **cbRemaining**, qui suivent dans cette structure.

</dd> <dt>

**guidSemantic**
</dt> <dd>

GUID qui détermine quels membres de l’Union sont présents ci-dessous. **guidSemantic** peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                           | Signification                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Détermine si l’exécution pas à pas unique doit être effectuée par le débogueur. Seul le membre **fStopOnOtherSide** de l’Union est présent ci-dessous.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Détermine si les données RPC triées et les OpCodes de débogage sont passés au récepteur. Tous les membres de l’Union sont présents ci-dessous, à l’exception de **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Si la **valeur est true**, le pas à pas est exécuté par le débogueur et il doit sortir du serveur et continuer l’exécution une fois que l’autre côté est atteint. Dans le cas contraire, l’exécution pas à pas n’est pas effectuée et l’exécution du débogueur s’arrête de l’autre côté.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Valeur qui autorise la spécification d’une série d’opérations. **wDebuggingOpCode** peut prendre l’une des valeurs suivantes :



| Valeur                                                                             | Signification                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Pas d'opération.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Si cette valeur est définie, la sémantique d’une seule étape est identique à celle de **fStopOnOtherSide** lorsqu’elle est définie sur **true**.<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Remplissage. Ne pas utiliser.

</dd> <dt>

**padding**
</dt> <dd>

Remplissage. Ne pas utiliser.

</dd> <dt>

**libéré**
</dt> <dd>

Taille, en octets, des données dans **rgbData**.

</dd> <dt>

**guidExtent**
</dt> <dd>

**GUID** qui détermine le type de données dans **rgbData**. **guidExtent** peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                           | Signification                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** est un pointeur d’interface marshalé.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Mémoire tampon d' **octets** utilisée pour passer des données com triées par RPC entre les débogueurs client et serveur. Le contenu de **rgbData** est déterminé par le **GUID** dans **guidExtent**.



| Valeur guidExtent                     | contenu rgbData                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Pointeur d’interface marshalé qui résulte de l’appel de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface). Le pointeur marshalé est converti en son pointeur d’interface correspondant à l’aide de [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Les membres de cette structure ont un alignement sur 1 octet et sont toujours transmis dans l’ordre d’octet avec primauté des octets de poids faible (Little-endian).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORPC \_ dbg \_ tout**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





