---
description: Ouvre un magasin de certificats spécifié.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120805"
---
# <a name="storeopen-method"></a>Store. Open, méthode

\[La méthode **Open** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Open** ouvre un [*magasin de certificats*](../secgloss/c-gly.md)spécifié. Par défaut, l’emplacement du magasin \_ de l’utilisateur actuel CAPICOM \_ \_ et CAPICOM \_ My \_ Store Store sont ouverts en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StoreLocation* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [ \_ \_ emplacement du magasin CAPICOM](capicom-store-location.md) qui indique l’emplacement du magasin à ouvrir. La valeur par défaut est le magasin de l' \_ utilisateur actuel CAPICOM \_ \_ . Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**magasin d’utilisateurs de CAPICOM \_ active \_ Directory \_ \_**</dt> </dl> | Le magasin est un magasin de Active Directory. Aucune erreur ne sera générée si un magasin de Active Directory est ouvert en lecture/écriture, mais que les modifications apportées au magasin ne seront pas conservées. Impossible d’ajouter ou de supprimer des certificats dans des magasins de Active Directory.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**magasin de l' \_ utilisateur actuel CAPICOM \_ \_**</dt> </dl>                             | Le magasin est un magasin de l’utilisateur actuel. Un magasin de l’utilisateur actuel peut être un magasin en lecture/écriture. Si c’est le cas, les modifications apportées au contenu du magasin sont conservées.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**base de l' \_ ordinateur local CAPICOM \_ \_**</dt> </dl>                          | Le magasin est un magasin de l’ordinateur local. Les magasins d’ordinateurs locaux peuvent être des magasins de lecture/écriture uniquement si l’utilisateur dispose d’autorisations de lecture/écriture. Si l’utilisateur dispose d’autorisations de lecture/écriture et si le magasin est ouvert en lecture/écriture, les modifications apportées au contenu du magasin sont conservées.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_magasin mémoire CAPICOM \_**</dt> </dl>                                                | Le magasin est un magasin de mémoire. Les modifications apportées au contenu du magasin ne sont pas conservées.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_magasin d’utilisateurs de \_ carte à puce \_ CAPICOM \_**</dt> </dl>                   | Le magasin est le groupe de cartes à puce actuelles. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le nom du magasin de certificats système à ouvrir. La valeur par défaut est CAPICOM \_ My \_ Store. Si le magasin est ouvert à partir d’un script Web, le caractère de barre oblique inverse ( \\ ) n’est pas autorisé dans le nom. En plus des magasins définis par le système, les magasins définis par l’utilisateur peuvent être ouverts.

Ce paramètre peut être un magasin défini par l’utilisateur ou l’un des magasins de certificats système suivants.



| Valeur                                                                                                                                                                            | Signification                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**\_magasin d’autorités de certification CAPICOM \_**</dt> </dl>          | Magasin d’autorités de certification. Ce magasin est utilisé pour stocker les certificats intermédiaires de l’autorité de certification.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ My \_ Store**</dt> </dl>          | Mon magasin. Ce magasin est utilisé pour les certificats personnels d’un utilisateur.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**\_autre \_ magasin**</dt> </dl> | Magasin AddressBook. Ce magasin est utilisé pour conserver les certificats des autres.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**\_magasin racine CAPICOM \_**</dt> </dl>    | Magasin racine. Ce magasin est utilisé pour stocker l’autorité de certification racine et les certificats de confiance auto-signés.<br/> |



 

</dd> <dt>

*OpenMode* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération du mode d’ouverture de l' [ \_ entrepôt d’enregistrement \_ \_ CAPICOM](capicom-store-open-mode.md) qui indique le mode d’ouverture du magasin. La valeur par défaut est CAPICOM \_ Store \_ ouvert \_ en lecture \_ seule. Si le magasin est ouvert à partir d’un script Web, cette valeur est forcée à l’ouverture de la base de l' \_ emplacement de stockage \_ \_ \_ uniquement. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                           | Signification                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**\_ \_ \_ maximum \_ autorisé pour le magasin CAPICOM**</dt> </dl> | Ouvre le magasin en mode lecture/écriture si l’utilisateur dispose d’autorisations de lecture/écriture. Sinon, ouvrez le magasin en mode lecture seule.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**le magasin CAPICOM \_ est \_ ouvert \_ en lecture \_ seule**</dt> </dl>                   | Ouvrez le magasin en lecture seule.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**ouverture de la \_ \_ \_ lecture écriture du \_ magasin CAPICOM**</dt> </dl>                | Ouvrez le magasin en mode lecture/écriture.<br/>                                                                                     |



 

Les indicateurs suivants peuvent être combinés avec les valeurs du tableau précédent à l’aide d’une opération **or** logique.



| Valeur                                                                                                                                                                                                                              | Signification                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**le magasin CAPICOM \_ est \_ ouvert \_ \_ uniquement**</dt> </dl>          | Ouvrir les magasins existants uniquement ; ne créez pas de nouveau magasin. Introduit dans CAPICOM 2,0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**l’ouverture du \_ magasin \_ CAPICOM \_ inclut \_ Archived**</dt> </dl> | Incluez les certificats archivés lors de l’utilisation du magasin. Introduit dans CAPICOM 2,0.<br/>   |



 

Les magasins situés dans certains emplacements ne peuvent être ouverts qu’en mode lecture seule. Cela inclut tous les magasins dans CAPICOM \_ local \_ machine \_ Store pour lesquels l’utilisateur ne dispose pas d’autorisations en écriture. Toute tentative d’ouverture d’un magasin en tant que magasin de lecture/écriture sans accès et autorisations appropriés entraîne l’échec de la méthode **Open** . Les magasins de Active Directory peuvent être ouverts en tant que magasin de lecture/écriture sans échec de la méthode **Open** , mais les modifications apportées au magasin ne sont pas rendues persistantes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si cette méthode est appelée sur un magasin de cartes à puce, d’autres interfaces utilisateur de carte à puce peuvent être appelées.

> [!IMPORTANT]
> Lorsque cette méthode est appelée à partir d’un script Web, le script doit accéder aux certificats numériques sur l’ordinateur local. Si vous autorisez le script à accéder à vos certificats numériques, le site Web à partir duquel le script est exécuté aura également accès aux informations personnelles stockées dans les certificats. La première fois que cette méthode est appelée à partir d’un domaine particulier, une boîte de dialogue est générée dans laquelle l’utilisateur doit indiquer si l’accès aux certificats doit être autorisé. Les magasins ouverts à partir d’un script Web forcent automatiquement l’indicateur de l’ouverture de l’ouverture de l' \_ emplacement existant du magasin CAPICOM \_ \_ \_ .

 

Si *StoreLocation* est un **magasin d' \_ \_ utilisateurs de \_ carte \_ à puce** CAPICOM, *StoreName* est ignoré. Dans ce cas, CAPICOM lit tous les certificats de tous les lecteurs disponibles qui contiennent une carte à puce.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**Plus**](store-close.md)
</dt> </dl>

 

 
