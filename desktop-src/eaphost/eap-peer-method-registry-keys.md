---
title: Valeurs de registre de la méthode d’homologue EAP
description: En savoir plus sur les valeurs de Registre spécifiques requises pour les méthodes homologues EAP. Affichez une liste de valeurs de Registre et affichez des ressources supplémentaires disponibles.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee42360689a74b3cd11628e6114e80532000b95f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476635"
---
# <a name="eap-peer-method-registry-values"></a>Valeurs de registre de la méthode d’homologue EAP

Des valeurs de Registre spécifiques sont requises pour les méthodes homologues EAP.

## <a name="eap-peer-method-dll-paths"></a>Chemins DLL de la méthode d’homologue EAP

Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode homologue EAP standard.

**HKLM \\ System \\ CCS \\ services \\ \\ \\ *&lt; EAPHost méthodes de réfaut à l’EapTypeId &gt;* \\ * &lt;&gt;***

Par exemple, un chemin d' **accès d’installation** d’une méthode EAP donné un réécriture de « 311 » (indiquant que « Microsoft » est l’auteur) et un **EapTypeId** de « 40 », s’affichent comme suit.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ méthodes \\ 311 \\ 40**

Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode EAP étendue.

> [!Note]  
> les dll de méthodes EAP étendues sont prises en charge dans Windows Vista avec Service pack 1 (SP1) ou version ultérieure.

 

**HKLM \\ System \\ CCS \\ services \\ EAPHost \\ Methods ID d' \\ *&lt; auteur &gt;* \\ 254 \\ *&lt; ID &gt;* de service \\ * &lt; EapTypeId&gt;***

Par exemple, un chemin d’accès d’installation d’une méthode EAP donné un ID d' **auteur** « 311 » (indiquant que « Microsoft » est l’auteur), un **ID** de formulaire « 311 » et un **EapTypeId** de « 40 », s’affichent comme suit.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ méthodes \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Pour plus d’informations sur l’allocation des types de méthode EAP, consultez la section 6,2 de la [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valeurs de Registre

Les valeurs de registre des méthodes homologues EAPHost suivantes sont requises.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Les valeurs de Registre suivantes de la méthode d’homologue AP sont recommandées.

-   [Propriétés](#properties)

Les valeurs de registre de la méthode d’homologue AP suivantes sont facultatives.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Valeur constante | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ développer \_ SZ                                                                                                                                        |
| Description    | Chemin d’accès à la DLL qui contient l’implémentation de la boîte de dialogue de configuration utilisateur. Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de la \_ dll &gt;.dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Valeur constante | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| Type           | REG \_ développer \_ SZ                                                                                 |
| Description    | Chemin d’accès à la DLL de méthode EAP. Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de la \_ dll &gt;.dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Valeur constante | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| Type           | SZ de REG \_                                                              |
| Description    | Chaîne qui contient le nom convivial de la méthode EAP. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Valeur constante | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ développer \_ SZ                                                                                                                                      |
| Description    | Chemin d’accès à la DLL qui contient l’implémentation des fonctions d’identité de l’utilisateur. Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de la \_ dll &gt;.dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Valeur constante | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ développer \_ SZ                                                                                                                                                                                                            |
| Description    | Chemin d’accès à la DLL qui contient l’implémentation de l’interface utilisateur interactive utilisée pour obtenir les informations utilisateur lors de l’exécution de la méthode EAP. Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de la \_ dll &gt;.dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Valeur constante | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | \_valeur DWORD reg                                                                                                                                                                                                                                       |
| Description    | 1-pour récupérer les informations d’identification à l’aide de la boîte de dialogue mot de passe et domaine EAPHost générique. 0-pour utiliser une boîte de dialogue personnalisée. Si la boîte de dialogue générique est utilisée, les informations d’identification sont définies par la méthode [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) . |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog




| Valeur constante | PeerInvokeUsernameDialog | 
|----------------|--------------------------|
| Type | REG_DWORD | 
| Description | <ul><li>1-pour récupérer les informations d’identification à l’aide de la boîte de dialogue générique EAPHost User Name.</li><li>0-pour utiliser une boîte de dialogue personnalisée.</li></ul>Si la boîte de dialogue générique est utilisée, les informations d’identification sont définies par la méthode [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) . | 




 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Valeur constante | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| Type           | \_valeur DWORD reg                                                                                 |
| Description    | 0 si une boîte de dialogue d’interface utilisateur de configuration est implémentée pour cette méthode ; 1 si ce n’est pas le cas. |



 

### <a name="properties"></a>Propriétés



| Valeur constante | Propriétés                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | \_valeur DWORD reg                                                                                                                                                  |
| Description    | Les bits dans la valeur DWORD sont définis pour indiquer la prise en charge de la propriété. Pour obtenir la liste des valeurs prises en charge, consultez Propriétés de la [**méthode EAP**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[clés de registre de la méthode Authenticator EAP](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Configuration du Registre pour les types EAP étendus](registry-keys-for-eap-methods.md)
</dt> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 
