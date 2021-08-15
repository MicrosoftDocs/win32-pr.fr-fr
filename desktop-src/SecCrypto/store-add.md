---
description: Ajoute un objet certificat à un magasin de certificats ouvert.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f90d95184fd789530831628cb6e121e32ce258d4541769c47926d2fb46eb710c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897934"
---
# <a name="storeadd-method"></a>Store. Add, méthode

\[La méthode **Add** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Add** ajoute un objet [**certificat**](certificate.md) à un [*magasin de certificats*](../secgloss/c-gly.md)ouvert. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Certificat* \[ dans\]
</dt> <dd>

Expression qui correspond à un objet de [**certificat**](certificate.md) à ajouter au magasin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!IMPORTANT]
> Lorsque cette méthode est appelée sur un magasin système à partir d’un script Web, le script doit accéder aux certificats numériques sur l’ordinateur local. Si vous autorisez le script à accéder à vos certificats numériques, le site Web à partir duquel le script est exécuté aura également accès aux informations personnelles stockées dans les certificats. La première fois que cette méthode est appelée à partir d’un domaine particulier, une boîte de dialogue est générée dans laquelle l’utilisateur doit indiquer si l’accès aux certificats doit être autorisé.

 

Si le magasin n’est pas ouvert en mode lecture/écriture, cette méthode échoue. Bien que cette méthode puisse être utilisée avec les magasins de mémoire, toute modification apportée à un magasin de mémoire n’est pas conservée lors de la fermeture de la Banque.

Si le certificat ajouté au magasin est le même que celui qui existe déjà, la méthode **Add** supprime le certificat existant du magasin, puis ajoute le nouveau certificat. Le nouveau certificat hérite des propriétés du certificat existant.

## <a name="requirements"></a>Configuration requise



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

 

 
