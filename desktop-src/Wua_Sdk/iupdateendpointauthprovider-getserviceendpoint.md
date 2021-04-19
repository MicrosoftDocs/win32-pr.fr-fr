---
description: Demande un point de terminaison utilisé pour se connecter à un service.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'IUpdateEndpointProvider :: GetServiceEndpoint, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536120"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>IUpdateEndpointProvider :: GetServiceEndpoint, méthode

Demande un point de terminaison utilisé pour se connecter à un service.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ServiceId* \[ dans\]
</dt> <dd>

Identifie le service à mettre à jour.

</dd> <dt>

*endpointType* \[ dans\]
</dt> <dd>

Identifie le type de point de terminaison implémenté par le service.

L’énumération [**UpdateEndpointType**](updateendpointtype.md) définit les constantes suivantes.

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**


</dt> <dd>

Point de terminaison client-serveur utilisé pour se connecter au service de mise à jour.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**


</dt> <dd>

Point de terminaison de création de rapports utilisé lorsque le client signale les résultats des analyses, des téléchargements et des réinstallations dans le service de mise à jour

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**


</dt> <dd>

Point de terminaison de Self-Update utilisé lorsque l’ordinateur client contacte un service de mise à jour pour déterminer s’il existe une nouvelle version du logiciel client de l’agent Windows Update.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**


</dt> <dd>

Point de terminaison de réglementation utilisé lorsque l’ordinateur client contacte le service de régulation pour agir sur une mise à jour particulière applicable à l’ordinateur cible.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**


</dt> <dd>

Simple-Targeting endoint utilisé uniquement avec les services privés (serveurs WSUS dans les environnements d’entreprise).

</dd> </dl> </dd> <dt>

*proxySettings* \[ dans\]
</dt> <dd>

Identifie les paramètres utilisés lors de la connexion à un serveur proxy.

</dd> <dt>

*hUserToken* \[ dans\]
</dt> <dd>

Contient un objet de handle de jeton qui représente l’utilisateur. Le fournisseur de points de terminaison utilise ce jeton pour déterminer les paramètres de proxy et les informations d’identification à utiliser.

</dd> <dt>

*fRefreshOnline* \[ dans\]
</dt> <dd>

Indique que Weather WUA demande un nouveau jeton. La valeur true indique qu’un nouveau jeton est demandé. False indique qu’un nouveau jeton ou un jeton mis en cache est demandé. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*pbstrEndpointLoc* \[ à\]
</dt> <dd>

Spécifiez l’URL utilisée pour communiquer avec le service. Par exemple, pour un point de terminaison sécurisés-Server, il s’agit de l’URL du service du serveur client. Pour plus d'informations, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite. Sinon, retourne un code d’erreur COM ou Windows.

## <a name="remarks"></a>Notes

WUA affecte généralement la valeur false au paramètre *fRefreshOnline* lorsque cette méthode est appelée pour la première fois, puis, si une erreur de connexion se produit, WUA définit ce paramètre sur true lorsque la méthode est à nouveau appelée. Toutefois, l’implémentation de cette méthode peut demander un nouveau jeton auprès d’un service d’émission de jeton de sécurité (STS) ou fournir un jeton mis en cache à tout moment.

Si le point de terminaison n’a pas besoin d’authentification, l’appelant peut se connecter au service en utilisant uniquement l’URL spécifiée par le paramètre *pbstrEndpointLoc* .

Si le point de terminaison a besoin d’une authentification, l’appelant peut utiliser l’URL spécifiée par le paramètre *pbstrEndpointLoc* et les données fournies par les autres paramètres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUpdateEndpointProvider**](iupdateendpointprovider.md)
</dt> </dl>

 

 




