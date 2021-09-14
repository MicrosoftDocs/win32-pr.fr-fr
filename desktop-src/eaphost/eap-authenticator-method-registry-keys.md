---
title: valeurs de registre de la méthode Authenticator EAP
description: en savoir plus sur les valeurs de registre de la méthode EAP Authenticator. Ces valeurs de Registre spécifiques sont requises pour les méthodes d’authentificateur EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118405"
---
# <a name="eap-authenticator-method-registry-values"></a>valeurs de registre de la méthode Authenticator EAP

Des valeurs de Registre spécifiques sont requises pour les méthodes d’authentificateur EAP.

## <a name="eap-authenticator-method-dll-paths"></a>chemins d’accès de la DLL de méthode Authenticator EAP

Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode d’authentificateur EAP standard.

**HKLM \\ System \\ CCS \\ services \\ \\ \\ *&lt; EAPHost méthodes de réfaut à l’EapTypeId &gt;* \\ * &lt;&gt;***

Par exemple, le chemin d’accès d’installation d’une méthode de l’authentificateur EAP, en fonction de la **valeur de l’identificateur d’auteur «** 311 » (indiquant que « Microsoft » est l’auteur) et d’un **EapTypeId** de « 40 », s’affiche comme suit.

**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ méthodes \\ 311 \\ 40**

Le chemin d’accès suivant spécifie l’emplacement du Registre pour les dll de méthode d’authentificateur EAP étendue.

**HKLM \\ System \\ CCS \\ services \\ EAPHost \\ Methods ID d' \\ *&lt; auteur &gt;* \\ 254 \\ *&lt; ID &gt;* de \\ * &lt; la méthode&gt;***

Par exemple, un chemin d’accès d’installation d’une méthode d’authentificateur EAP donné un **ID** d' **auteur** « 311 » (indiquant que « Microsoft » est l’auteur), un identificateur de formulaire « 311 » et un **EapTypeId** de « 40 », s’affiche comme suit.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ méthodes \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Pour plus d’informations sur l’allocation des types de méthode EAP, consultez la section 6,2 de la [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Valeurs de Registre

Les valeurs de registre de la méthode d’authentificateur suivantes sont requises.

-   [AuthenticatorDllPath](#authenticatordllpath)
-   [AuthenticatorFriendlyName](#authenticatorfriendlyname)

Outre les valeurs de Registre ci-dessus, la valeur de registre de la méthode d’authentificateur suivante est recommandée.

-   [Propriétés](#properties)

Les valeurs de registre de la méthode d’authentificateur restante sont facultatives.

-   [ConfigCLSID](#configclsid)
-   [StandaloneSupported](#standalonesupported)

## <a name="authenticatordllpath"></a>AuthenticatorDllPath



| Valeur constante | AuthenticatorDllPath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Type           | REG \_ développer \_ SZ                                                                                               |
| Description    | Chemin d’accès à la DLL de méthode de l’authentificateur EAP. Par exemple,% SystemRoot% \\ system32 \\ &lt; nom \_ de la \_ dll &gt;.dll. |



 

## <a name="authenticatorfriendlyname"></a>AuthenticatorFriendlyName



| Valeur constante | AuthenticatorFriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| Type           | SZ de REG \_                                                                            |
| Description    | Chaîne qui contient le nom convivial de la méthode d’authentificateur EAP. |



 

## <a name="configclsid"></a>ConfigCLSID



| Valeur constante | ConfigCLSID                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Type           | SZ de REG \_                                                                                                                               |
| Description    | Chaîne qui contient le GUID de la classe de configuration pour cette méthode de l’authentificateur, au format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} |



 

## <a name="properties"></a>Propriétés



| Valeur constante | Propriétés                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type           | \_valeur DWORD reg                                                                                                                                                  |
| Description    | Les bits dans la valeur DWORD sont définis pour indiquer la prise en charge de la propriété. Pour obtenir la liste des valeurs prises en charge, consultez Propriétés de la [**méthode EAP**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>StandaloneSupported



| Valeur constante | StandaloneSupported                                             |
|----------------|-----------------------------------------------------------------|
| Type           | \_valeur DWORD reg                                                      |
| Description    | 0 s’il s’agit d’une méthode d’authentificateur autonome ; 1 si ce n’est pas le cas. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clés de registre de la méthode d’homologue EAP](eap-peer-method-registry-keys.md)
</dt> <dt>

[Configuration du Registre pour les types EAP étendus](registry-keys-for-eap-methods.md)
</dt> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




