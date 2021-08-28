---
description: Importe des certificats à partir d’un fichier dans le magasin.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b39c2be625ff88869d27e6210e49496352af868c73557d2657c509fd0e79f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897789"
---
# <a name="storeload-method"></a>Store. Load, méthode

\[La méthode de **chargement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Load** importe des certificats à partir d’un fichier dans le magasin.

## <a name="syntax"></a>Syntaxe


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Chaîne qui contient le chemin d’accès à un fichier. cer,. SST,. SPC,. p7s ou. pfx, ou un fichier signé Authenticode.

</dd> <dt>

*Mot de passe* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le mot de passe en texte clair dans le fichier. Jusqu’à 32 caractères Unicode, y compris un caractère null de fin, peuvent être utilisés pour le mot de passe. Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [**indicateur de \_ \_ stockage \_ de clé CAPICOM**](capicom-key-storage-flag.md) qui définit les indicateurs de stockage de clé. La valeur par défaut est le \_ \_ stockage par clé CAPICOM \_ par défaut. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                           | Signification                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**\_ \_ \_ valeur par défaut du stockage de la clé CAPICOM**</dt> </dl>                       | Stockage de clé par défaut.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**\_espace de stockage de clé CAPICOM \_ \_ exportable**</dt> </dl>              | La clé peut être exportée.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**\_clé CAPICOM \_ \_ protégée par l’utilisateur \_**</dt> </dl> | La clé est protégée par l’utilisateur.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si la méthode **Load** est appelée sur un magasin de mémoire, tous les conteneurs de clé créés sont supprimés lors de la suppression du magasin de mémoire. Par exemple, si un fichier. pfx est chargé dans un magasin de mémoire et ajouté ultérieurement à un magasin système (tel que le magasin My) à partir du magasin de mémoire, le certificat du magasin My ne contient pas de clé. Dans ce cas, le fichier. pfx doit être chargé directement dans le magasin My.

Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.

Si le mot de passe ne parvient pas à déchiffrer le fichier de clé privée, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) par défaut doit être interrogé. Si le fournisseur de services de chiffrement par défaut est le fournisseur de services de chiffrement de base Microsoft et que l’opération de déchiffrement échoue, l’opération de déchiffrement doit être retentée avec le fournisseur de services de chiffrement fort Microsoft ou le fournisseur de services de chiffrement amélioré

Si le certificat en cours de chargement dans le magasin est le même que celui qui existe déjà, la méthode **Load** supprime le certificat existant du magasin, puis ajoute le nouveau certificat. Le nouveau certificat héritera des propriétés du certificat existant. Le conteneur de clé privée existant est remplacé par le nouveau conteneur de clé privée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> </dl>

 

 
