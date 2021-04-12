---
title: Point d’entrée VirtualChannelGetInstance
description: Appelé pour que le plug-in crée une instance de l’interface IWTSPlugin pour tous les plug-ins implémentés par la DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Point d’entrée VirtualChannelGetInstance Services Bureau à distance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384271"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Point d’entrée VirtualChannelGetInstance

Appelé pour que le plug-in crée une instance de l’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour tous les plug-ins implémentés par la dll.

> [!Note]
>
> Cette fonction est implémentée par le plug-in et doit être exportée par nom afin qu’une application puisse utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à la fonction.
>
> Le prototype de cette fonction n’est contenu dans aucun fichier d’en-tête public. vous devez donc le déclarer exactement comme indiqué.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*REFIID* \[ dans\]
</dt> <dd>

Spécifie le type d’interface à retourner. Il doit s’agir de l' **IID \_ IWTSPlugin**.

</dd> <dt>

*pNumObjs* \[ in, out\]
</dt> <dd>

Adresse d’une variable **ULong** qui reçoit le nombre d’interfaces récupérées.

</dd> <dt>

*ppObjArray* \[ à\]
</dt> <dd>

Adresse d’un tableau de pointeurs qui reçoit les pointeurs d’interface. Si ce paramètre a la **valeur null**, l’implémentation doit placer le nombre de plug-ins implémentés par la dll dans le paramètre *pNumObjs* . Cela permet à l’appelant d’allouer le tableau de taille approprié pour *ppObjArray*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si ce point d’entrée est correctement exécuté, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

