---
description: Représente la clé privée associée à un certificat.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Objet PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120849"
---
# <a name="privatekey-object"></a>Objet PrivateKey

\[L’objet **PrivateKey** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **PrivateKey** représente la [*clé privée*](../secgloss/p-gly.md) associée à un certificat.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **PrivateKey** est utilisé pour effectuer les tâches suivantes :

-   Récupérez les informations relatives à la clé privée.
-   Ouvrez le conteneur de clé privée.
-   Supprimez la clé privée.

## <a name="members"></a>Membres

L’objet **PrivateKey** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **PrivateKey** a ces méthodes.



| Méthode                                                  | Description                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Supprimer**](privatekey-delete.md)                     | Supprime le conteneur de clé privée référencé par l’objet **PrivateKey** .<br/>                                                                                |
| [**IsAccessible**](privatekey-isaccessible.md)         | Récupère une valeur booléenne qui indique si la clé privée est accessible par l’utilisateur. Si la valeur est true, l’utilisateur peut accéder à la clé privée.<br/>                 |
| [**IsExportable**](privatekey-isexportable.md)         | Récupère une valeur booléenne qui indique si la clé privée peut être exportée. Si la valeur est true, la clé privée peut être exportée.<br/>                               |
| [**IsHardwareDevice**](privatekey-ishardwaredevice.md) | Récupère une valeur booléenne qui indique si la clé privée est stockée sur un périphérique matériel. Si la valeur est true, la clé privée est stockée sur un périphérique matériel.<br/> |
| [**IsMachineKeyset**](privatekey-ismachinekeyset.md)   | Récupère une valeur booléenne qui indique si la clé privée est une clé d’ordinateur. Si la valeur est true, la clé privée est une clé d’ordinateur.<br/>                             |
| [**IsProtected**](privatekey-isprotected.md)           | Récupère une valeur booléenne qui indique si la clé privée est protégée. Si la valeur est true, la clé privée est protégée.<br/>                                     |
| [**IsRemovable**](privatekey-isremovable.md)           | Récupère une valeur booléenne qui indique si la clé privée est sur un appareil amovible. Si la valeur est true, la clé privée se trouve sur un périphérique amovible.<br/>             |
| [**Ouvrir**](privatekey-open.md)                         | Accède à un conteneur de clé existant.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriétés

L’objet **PrivateKey** a ces propriétés.



| Propriété                                                                 | Type d’accès          | Description                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [**ContainerName**](privatekey-containername.md)<br/>             | Lecture seule<br/> | Récupère une chaîne qui contient le nom du conteneur de clé privée. Il s’agit de la propriété par défaut.<br/> |
| [**KeySpec**](privatekey-keyspec.md)<br/>                         | Lecture seule<br/> | Récupère la spécification de clé.<br/>                                                               |
| [**ProviderName**](privatekey-providername.md)<br/>               | Lecture seule<br/> | Récupère une chaîne qui contient le nom du fournisseur de services de chiffrement.<br/>                                          |
| [**ProviderType**](privatekey-providertype.md)<br/>               | Lecture seule<br/> | Récupère une valeur d’énumération qui spécifie le type de fournisseur.<br/>                            |
| [**UniqueContainerName**](privatekey-uniquecontainername.md)<br/> | Lecture seule<br/> | Récupère une chaîne qui contient le nom unique du conteneur de clé privée.<br/>                        |



 

## <a name="remarks"></a>Notes

L’objet **PrivateKey** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **PrivateKey** est CAPICOM. PrivateKey. 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
