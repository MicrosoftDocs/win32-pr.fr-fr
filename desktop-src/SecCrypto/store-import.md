---
description: La méthode d’importation copie dans un magasin de certificats ouvert le contenu d’un magasin de certificats précédemment exporté. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d36dfcd7e0273dd76e15b204fa9976f6732f53252242b70a61d2089e853b611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972593"
---
# <a name="storeimport-method"></a>Store. Import, méthode

\[La méthode d' **importation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode d' **importation** copie dans un [*magasin de certificats*](../secgloss/c-gly.md) ouvert le contenu d’un magasin de certificats précédemment exporté. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EncodedStore* \[ dans\]
</dt> <dd>

Chaîne qui contient les certificats encodés à importer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!IMPORTANT]
> Lorsque cette méthode est appelée à partir d’un script Web, le script doit accéder aux certificats numériques sur l’ordinateur local. Si vous autorisez le script à accéder à vos certificats numériques, le site Web à partir duquel le script est exécuté aura également accès aux informations personnelles stockées dans les certificats. La première fois que cette méthode est appelée à partir d’un domaine particulier, une boîte de dialogue est générée dans laquelle l’utilisateur doit indiquer si l’accès aux certificats doit être autorisé.

 

Si le magasin n’est pas ouvert avec l’autorisation de lecture/écriture, cette méthode échoue. Bien que cette méthode puisse être utilisée avec les magasins de mémoire, toute modification apportée à un magasin de mémoire n’est pas conservée lors de la fermeture de la Banque.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
