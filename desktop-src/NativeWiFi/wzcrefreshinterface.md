---
description: Actualise les informations d’interface pour une interface de réseau local sans fil spécifique.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: WZCRefreshInterface, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119333"
---
# <a name="wzcrefreshinterface-function"></a>WZCRefreshInterface fonction)

\[**WZCRefreshInterface** n’est pas pris en charge à partir de Windows Vista et Windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

La fonction **WZCRefreshInterface** actualise les informations d’interface pour une interface de réseau local sans fil spécifique.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrvAddr* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction. Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est appelé sur l’ordinateur local.

Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.

</dd> <dt>

*dwInFlags* \[ dans\]
</dt> <dd>

Ensemble de champs à actualiser, ainsi que des actions d’actualisation spécifiques à entreprendre. Il s’agit d’un masque de masque qui peut contenir n’importe quelle combinaison des indicateurs suivants.



| Valeur                                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ DESCr**</dt> <dt>0x00010000</dt> </dl>             | Actualisez la description de l’interface pour une interface de réseau local sans fil.<br/> La description de l’interface actualisée peut être récupérée en appelant la fonction [**WZCQueryInterface**](wzcqueryinterface.md) avec le bit **\_ descr INTF** défini dans le paramètre *dwInFlags* . La description de l’interface est retournée dans le membre **wszDescr** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* retourné par la fonction **WZCQueryInterface** .<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | Actualiser les informations de média NDIS pour une interface de réseau local sans fil.<br/> Les informations de média NDIS actualisées peuvent être récupérées en appelant la fonction [**WZCQueryInterface**](wzcqueryinterface.md) avec le bit **INTF \_ NDISMEDIA** défini dans le paramètre *dwInFlags* . Les informations de média NDIS sont retournées dans les membres **ulMediaState**, **ulMediaType** et **ulPhysicalMediaType** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* retourné par la fonction **WZCQueryInterface** .<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ Tous les \_ OID**</dt> <dt>0xFFF00000</dt> </dl>   | Actualiser tous les OID NDIS pour une interface de réseau local sans fil. Cette option actualise la plupart des données pour une interface de réseau local sans fil.<br/> Les informations actualisées peuvent être récupérées en appelant la fonction [**WZCQueryInterface**](wzcqueryinterface.md) .<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ entrée INTF**](intf-entry.md) qui contient la clé de l’interface à actualiser.

</dd> <dt>

*pdwOutFlags* \[ à\]
</dt> <dd>

Ensemble de champs qui ont été correctement actualisés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR de la \_ \_ Corbeille**</dt> </dl>     | Les blocs de contrôle de stockage ont été détruits. Cette erreur est retournée si le service de configuration sans fil Zero n’a pas initialisé d’objets internes.<br/>                                                                                                                      |
| <dl> <dt>**\_fichier d' \_ erreur \_ introuvable**</dt> </dl>   | Le système ne peut pas trouver le fichier spécifié. Cette erreur est retournée si le GUID dans le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* ne correspond à aucune des interfaces de réseau local sans fil sur l’ordinateur local. <br/> |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl> | Un paramètre est incorrect. Cette erreur est retournée si le paramètre *pIntf* a la **valeur null**. Cette erreur est retournée si le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* a la **valeur null**. <br/>                            |
| <dl> <dt>**\_état RPC**</dt> </dl>               | Divers codes d’erreur.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Notes

Le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* doit contenir un GUID d’interface pour une interface de réseau local sans fil. Une liste d’interfaces de réseau local sans fil peut être récupérée en appelant la fonction [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

> [!Note]  
> le fichier d’en-tête *Wzcsapi. h* et le fichier de bibliothèque d’importation *Wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.

 

## <a name="requirements"></a>Spécifications



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

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**\_entrée INTF**](intf-entry.md)
</dt> </dl>

 

 




