---
description: Fournit des informations détaillées pour une interface de réseau local sans fil gérée par le service de configuration sans fil de zéro.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: WZCQueryInterface, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3dd7ce876501486b9bec4dbad63ce5812b910b32b9dcdaa1eb80aff3e7cc415e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797409"
---
# <a name="wzcqueryinterface-function"></a>WZCQueryInterface fonction)

\[**WZCQueryInterface** n’est plus pris en charge à partir de Windows Vista et Windows Server 2008. Utilisez à la place la fonction [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) . Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md). \]

La fonction **WZCQueryInterface** fournit des informations détaillées pour une interface de réseau local sans fil gérée par le service de configuration sans fil Zero.

Fournit des informations détaillées sur une interface donnée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrvAddr* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction. Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est interrogé sur l’ordinateur local.

Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.

</dd> <dt>

*dwInFlags* \[ dans\]
</dt> <dd>

Champs à interroger. Il s’agit d’un masque de masque qui peut contenir n’importe quelle combinaison des indicateurs suivants.



| Valeur                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | Retournez la valeur du membre **dwDynFlags** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ DESCr**</dt> <dt>0x00010000</dt> </dl>                      | Retournez la valeur du membre **wszDescr** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | Retournez les valeurs pour les membres **ulMediaState**, **ulMediaType** et **ulPhysicalMediaType** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ PREFLIST**</dt> <dt>0x00040000</dt> </dl>             | Retourne la liste par défaut des réseaux dans le membre **rdStSSIDList** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ FONCTIONNALITÉS**</dt> <dt>0x00080000</dt> </dl> | Retournez les valeurs pour les membres **dwCapabilities** et **rdNicCapabilities** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_ INFRAMODE**</dt> <dt>0x00200000</dt> </dl>          | Retournez la valeur du membre **nInfraMode** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/> Le membre **nInfraMode** est valide uniquement dans certains États de contexte d’interface.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ AUTHMODE**</dt> <dt>0x00400000</dt> </dl>             | Retournez la valeur du membre **nAuthMode** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* . <br/> Le membre **nAuthMode** est valide uniquement dans certains États de contexte d’interface.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ WEPSTATUS**</dt> <dt>0x00800000</dt> </dl>          | Retournez la valeur du membre **nWepStatus** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* . <br/> Le membre **nWepStatus** est valide uniquement dans certains États de contexte d’interface.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Retournez la valeur du membre **rdSSID** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/> Le membre **rdSSID** est valide uniquement dans certains États de contexte d’interface.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Retournez la valeur du membre **rdBSSID** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/> Le membre **rdBSSID** est valide uniquement dans certains États de contexte d’interface.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | Retourne la liste visible des réseaux dans le membre **rdBSSIDList** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .<br/> Le membre **rdBSSIDList** est valide uniquement dans certains États de contexte d’interface.<br/> |



 

</dd> <dt>

*pIntf* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers la clé de l’interface à interroger. Lors de la sortie, pointeur vers les données d’interface demandées. Ce paramètre est un pointeur vers une structure d' [**\_ entrée INTF**](intf-entry.md) .

</dd> <dt>

*pdwOutFlags* \[ à\]
</dt> <dd>

Un ensemble de champs correctement récupérés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.



| Code de retour                                                                                               | Description                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR de la \_ \_ Corbeille**</dt> </dl>      | Les blocs de contrôle de stockage ont été détruits. Cette erreur est retournée si le service de configuration sans fil Zero n’a pas initialisé d’objets internes.<br/>                                                                                                                      |
| <dl> <dt>**\_fichier d' \_ erreur \_ introuvable**</dt> </dl>    | Le système ne peut pas trouver le fichier spécifié. Cette erreur est retournée si le GUID dans le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* ne correspond à aucune des interfaces de réseau local sans fil sur l’ordinateur local. <br/> |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>  | Un paramètre est incorrect. Cette erreur est retournée si le paramètre *pIntf* a la **valeur null**. Cette erreur est retournée si le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* a la **valeur null**. <br/>                            |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl> | Mémoire disponible insuffisante pour traiter cette demande et allouer de la mémoire pour les résultats de la requête.<br/>                                                                                                                                                                       |
| <dl> <dt>**\_état RPC**</dt> </dl>                | Divers codes d’erreur.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Remarques

Le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* doit contenir un GUID d’interface pour une interface de réseau local sans fil. Une liste d’interfaces de réseau local sans fil peut être récupérée en appelant la fonction [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

Les membres suivants de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe *pIntf* doit avoir la valeur 0 avant un appel à la fonction **WZCQueryInterface** : **RdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** et **rdCtrlData**.

Le service de configuration sans fil Zero automotically ne met pas à jour l’état du support, même lorsque des événements Media Connected et Disconnected sont reçus. Une application doit forcer l’actualisation de l’état d’un média en appelant la fonction [**WZCRefreshInterface**](wzcrefreshinterface.md) avant d’appeler la fonction **WZCQueryInterface** si l’état du média NDIS doit être demandé (le \_ bit INTF NDISMEDIA est défini dans le paramètre *dwInFlags* ).

Lorsque le paramètre *dwInFlags* contient **INTF \_ BSSIDLIST**, la fonction **WZCQueryInterface** ne définit pas l' *dwOutFlags* avec **INTF \_ BSSIDLIST** si la liste visible des réseaux est vide. Lorsque le paramètre *dwInFlags* contient **INTF \_ SSID**, la fonction **WZCQueryInterface** ne définit pas le *dwOutFlags* avec **INTF \_ SSID** si aucun SSID n’est disponible.

Si la fonction **WZCQueryInterface** retourne \_ une erreur, l’appelant doit appeler la fonction [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) avec le paramètre *pIntf* pour libérer les mémoires tampons internes allouées pour les données retournées une fois que ces informations ne sont plus nécessaires. Cela libère les mémoires tampons utilisées par les membres **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** et **rdCtrlData** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .

> [!Note]  
> le fichier d’en-tête *Wzcsapi. h* et le fichier de bibliothèque d’importation *Wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                         |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_entrée INTF**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
