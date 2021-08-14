---
title: Structure ORPC_DBG_ALL
description: La \_ structure ORPC dbg \_ All est utilisée pour passer des paramètres aux méthodes de l’interface IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- Structure COM ORPC_DBG_ALL
- Pointeur de structure LPORPC_DBG_ALL COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 359e3b3ec2530917c6a502da90ea86771238319687f8dcf8e9b7862e4ddf1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310303"
---
# <a name="orpc_dbg_all-structure"></a>ORPC \_ dbg \_ tout (structure)

La structure **ORPC \_ dbg \_ All** est utilisée pour passer des paramètres aux méthodes de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]  
> Chaque méthode de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) utilise une combinaison différente des membres ci-dessous. Si un membre n’est pas indiqué comme utilisé par une méthode, il n’est pas défini lorsqu’il est passé à cette méthode.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>Membres

<dl> <dt>

**pSignature**
</dt> <dd>

Pointeur vers une mémoire tampon d' **octets** qui contient :

-   Quatre premiers octets : caractères ASCII « MARB » dans l’ordre de mémoire plus élevé.
-   16 octets suivants : **GUID** qui identifie la notification appelée. Il contient l’un des éléments suivants :
    1.  [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11
-   Quatre octets suivants : réservé pour une utilisation ultérieure.

> [!Note]
>
> Utilisé par toutes les méthodes de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

</dd> <dt>

**pMessage**
</dt> <dd>

Pointeur vers une structure [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) qui contient des informations de marshaling de données RPC.

> [!Note]
>
> Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**REFIID**
</dt> <dd>

Pointeur vers l’IID de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]
>
> Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pChannel**
</dt> <dd>

Pointeur vers l’interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) de l’implémentation du canal RPC com sur le serveur.

> [!Note]
>
> Utilisé par les méthodes [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Pointeur vers l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de l’objet impliqué dans l’appel de ce débogueur. Peut avoir la **valeur null**, mais cela réduit la fonctionnalité du débogueur.

> [!Note]
>
> Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)et [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .

 

</dd> <dt>

**pInterface**
</dt> <dd>

Pointeur vers l’interface COM de la méthode qui sera appelée par ce RPC. Ne doit pas avoir la **valeur null**.

> [!Note]
>
> Utilisé par les méthodes [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Doit avoir la **valeur null**.

> [!Note]
>
> Utilisé par les méthodes [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**signé**
</dt> <dd>

L’objectif de ce membre change pour chacune des notifications ci-dessous :

[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): nombre d’octets que le débogueur client transmet au débogueur de serveur. Si la valeur est zéro, aucune information n’est transmise.

[**ClientNotify**](iorpcdebugnotify-clientnotify.md): **HRESULT** du dernier RPC.

[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): nombre d’octets que le débogueur client transmet au débogueur de serveur. Si la valeur est zéro, aucune information n’est transmise.

> [!Note]
>
> Utilisé par les méthodes [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)et [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Pointeur vers une structure [**de \_ \_ mémoire tampon dbg ORPC**](orpc-dbg-buffer.md) qui contient les informations de débogage RPC marshalées. N’est pas défini si **cbBuffer** est égal à zéro.

> [!Note]
>
> Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

Longueur, en octets, des données vers lesquelles pointe **pvBuffer**.

> [!Note]
>
> Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

Nombre d’octets que le débogueur client transmet au débogueur de serveur. Si la valeur est zéro, aucune information n’est transmise. Cette valeur remplace la valeur retournée dans **HRESULT**.

> [!Note]
>
> Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .

 

</dd> <dt>

**reserved**
</dt> <dd>

Réservé. Ne pas utiliser.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ mémoire tampon dbg ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

