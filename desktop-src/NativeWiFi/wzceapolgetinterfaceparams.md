---
description: Obtient les paramètres de configuration EAPOL pour l’interface de réseau local sans fil spécifiée.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: WZCEapolGetInterfaceParams, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521924"
---
# <a name="wzceapolgetinterfaceparams-function"></a>WZCEapolGetInterfaceParams fonction)

\[**WZCEapolGetInterfaceParams** n’est plus pris en charge à compter de Windows Vista et de windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

La fonction **WZCEapolGetInterfaceParams** obtient les paramètres de configuration EAPOL pour l’interface de réseau local sans fil spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrvAddr* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction. Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est appelé sur l’ordinateur local.

Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.

</dd> <dt>

*pwszGuid* \[ dans\]
</dt> <dd>

GUID de l’interface pour laquelle les données doivent être récupérées.

</dd> <dt>

*dwSizeOfSSID* \[ dans\]
</dt> <dd>

Taille de l’identificateur réseau pour lequel les données doivent être récupérées.

</dd> <dt>

*pbSSID* \[ dans\]
</dt> <dd>

Pointeur vers l’identificateur réseau pour lequel les données doivent être récupérées.

</dd> <dt>

*pIntfParams* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**EAPOL \_ INTF \_ params**](eapol-intf-params.md) qui contient des paramètres d’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’erreur \_ de réussite si l’opération se termine correctement ; sinon, retourne l’un des codes d’erreur système Windows.

## <a name="remarks"></a>Notes

Si le **WZCEapolGetInterfaceParams** retourne \_ une erreur, l’appelant doit appeler [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) pour libérer les mémoires tampons internes allouées pour les données retournées une fois que ces informations ne sont plus nécessaires.

> [!Note]  
> Le fichier d’en-tête *wzcsapi. h* et le fichier de bibliothèque d’importation *wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                         |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
