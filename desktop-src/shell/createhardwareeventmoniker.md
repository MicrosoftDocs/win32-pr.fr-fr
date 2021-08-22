---
description: Crée un moniker qui représente un composant matériel et son gestionnaire d’événements associé. La lecture automatique utilise cette fonction pour permettre aux applications d’utiliser des événements de lecture automatique.
title: CreateHardwareEventMoniker fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 42f2da51bac93733a74113d3a567802975aca18be2a34f6fa349ff65349749c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460553"
---
# <a name="createhardwareeventmoniker-function"></a>CreateHardwareEventMoniker fonction)

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Crée un moniker qui représente un composant matériel et son gestionnaire d’événements associé. La lecture automatique utilise cette fonction pour permettre aux applications d’utiliser des événements de lecture automatique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CLSID* \[ dans\]
</dt> <dd>

Type : **REFCLSID**

ID de la classe à laquelle le moniker est lié.

</dd> <dt>

*pszEventHandler* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Nom du gestionnaire d’événements.

</dd> <dt>

*ppmoniker* \[ à\]
</dt> <dd>

Type : **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Adresse d’une variable pointeur qui reçoit le pointeur d’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Utilisez **CreateHardwareEventMoniker** lors de l’inscription d’applications en cours d’exécution afin que ces applications aient accès aux événements de lecture automatique. Pour utiliser des événements de lecture automatique dans des applications en cours d’exécution, vous devez d’abord créer un nouveau composant qui implémente l’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) . Initialisez cette interface avec la valeur InitCmdLine de l’entrée du gestionnaire particulier sous la clé des **gestionnaires** , car la lecture automatique n’appelle pas la méthode [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .

Vous devez appeler **CreateHardwareEventMoniker** pour obtenir un moniker qui représente votre composant et son gestionnaire d’événements. Ensuite, utilisez la valeur retournée dans le paramètre *ppmoniker* pour inscrire votre composant dans la table ROT (Running Object Table) comme indiqué dans l’exemple.

Notez que **CreateHardwareEventMoniker** n’est pas défini dans un fichier d’en-tête. Pour l’utiliser dans votre code, vous devez obtenir un handle vers le fichier Shsvcs.dll par le biais d’un appel à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Vous utilisez ensuite ce handle dans un appel à [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir une instance de la fonction **CreateHardwareEventMoniker** .

L’appel à [**IRunningObjectTable :: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) exige que vous entriez les informations **AppID** suivantes dans le registre.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
