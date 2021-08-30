---
title: PxeProviderRecvRequest fonction de rappel
description: Appelée lorsqu’une demande est reçue d’un client.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- fonction de rappel PxeProviderRecvRequest Windows les Services de déploiement
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dc2ef36c26e667e55870d38f450891e9e91134c297d09ba12157452e4d01442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098649"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>PxeProviderRecvRequest fonction de rappel

Appelée lorsqu’une demande est reçue d’un client. Cette fonction est inscrite en appelant la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec le paramètre *CallbackType* défini sur la **\_ \_ \_ demande de rappel PXE**.

## <a name="syntax"></a>Syntaxe


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hClientRequest* \[ dans\]
</dt> <dd>

Handle d’une demande reçue d’un client.

</dd> <dt>

*pPacket* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon qui contient le paquet reçu.

</dd> <dt>

*uPacketLen* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon vers laquelle pointe le paramètre *pPacket* .

</dd> <dt>

*pLocalAddress* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ adresse PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) qui contient l’adresse locale sur laquelle le paquet a été reçu.

</dd> <dt>

*pRemoteAddress* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ adresse PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) qui contient l’adresse source du paquet.

</dd> <dt>

*Pacte* \[ à\]
</dt> <dd>

Spécifie l’action que le système doit effectuer.



| Valeur                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> Environnement <dt>**PXE \_ E \_ NBP**</dt> <dt>1</dt> </dl>                | Le fournisseur a répondu à un client avec un paquet de réponse DHCP standard qui contient un chemin d’accès au programme de démarrage réseau. Le retour de cette action signifie que le fournisseur a terminé la demande du client en appelant la fonction [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) au moins une fois.<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> Environnement <dt>**PXE \_ BA \_ personnalisé**</dt> <dt>2</dt> </dl>       | Le fournisseur a répondu à un client à l’aide d’une réponse personnalisée qui n’est pas conforme aux spécifications DHCP. Le retour de cette action signifie que le fournisseur a terminé la demande du client en appelant la fonction [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) au moins une fois.<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> Environnement <dt>**PXE \_ BA \_ Ignorer**</dt> <dt>3</dt> </dl>       | Le fournisseur ne souhaite pas traiter la demande du client et la demande ne doit pas être transmise au fournisseur suivant. Toutes les ressources associées à la demande du client sont libérées et la demande du client est ignorée. Les fournisseurs peuvent également utiliser cette valeur s’ils reconnaissent le client mais que la demande est incorrecte.<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> Environnement <dt>**PXE \_ BA a \_ rejeté**</dt> <dt>4</dt> </dl> | Le fournisseur ne souhaite pas traiter la demande du client. Le système transmet la demande au fournisseur suivant dans la liste des fournisseurs inscrits. S’il s’agit du dernier fournisseur de la liste, toutes les ressources associées à la demande du client sont libérées et la demande du client est ignorée.<br/>                     |



 

</dd> <dt>

*pContext* \[ dans\]
</dt> <dd>

Valeur de contexte passée à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le fournisseur a correctement traité la demande du client, le rappel doit retourner la **\_ réussite** de l’erreur et l' **\_ \_ action de démarrage PXE** vers laquelle pointe le paramètre de *Pacte* contient l’action de démarrage appropriée pour cette demande. Si le fournisseur traitera la demande du client de manière asynchrone, le rappel doit retourner des **\_ e/s d’erreur \_ en attente** et appeler la fonction [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) lorsque la demande du client a été traitée. En cas d’échec, un code d’erreur approprié doit être retourné et le système se poursuivra comme si l’action de démarrage **\_ \_ rejetée par PXE BA** avait été spécifiée.

## <a name="remarks"></a>Remarques

Le type de paquets détectés par un fournisseur peut être modifié à l’aide de la fonction [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows serveur 2008, Windows server 2003 avec les \[ applications de bureau SP2 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Fonctions du serveur des services de déploiement](windows-deployment-services-server-functions.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





