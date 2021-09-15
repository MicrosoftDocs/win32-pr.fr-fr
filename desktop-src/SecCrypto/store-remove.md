---
description: La méthode Remove supprime un certificat d’un magasin de certificats ouvert. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove (méthode)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413452"
---
# <a name="storeremove-method"></a>Store. Remove (méthode)

\[La méthode **Remove** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Remove** supprime un [*certificat*](../secgloss/c-gly.md) d’un [*magasin de certificats*](../secgloss/c-gly.md)ouvert. Cette méthode peut uniquement être utilisée avec un magasin qui a été ouvert avec l’autorisation de lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Certificat* \[ dans\]
</dt> <dd>

Expression qui correspond à une instance d’un objet de [**certificat**](certificate.md) à supprimer du magasin.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

> [!IMPORTANT]
> Lorsque cette méthode est appelée à partir d’un script Web, le script doit supprimer des certificats numériques de l’ordinateur local. Autoriser les sites Web non approuvés à supprimer des certificats numériques est un risque pour la sécurité. Une boîte de dialogue qui vous demande si le site Web peut supprimer des certificats apparaît lorsque cette méthode est appelée pour la première fois. Si vous autorisez l’application à supprimer des certificats et que vous sélectionnez ne plus afficher cette boîte de dialogue, la boîte de dialogue n’apparaît plus pour les scripts qui suppriment les certificats dans ce domaine. Toutefois, les scripts en dehors de ce domaine qui tentent de supprimer des certificats entraînent l’affichage de cette boîte de dialogue. Si vous n’autorisez pas le script à supprimer des certificats et que vous sélectionnez ne plus afficher cette boîte de dialogue, les scripts de ce domaine ne seront pas autorisés à supprimer des certificats.

 

Lorsque vous supprimez un certificat d’un magasin, vous devez d’abord supprimer la clé privée associée au certificat.

Si le magasin n’est pas ouvert avec l’autorisation de lecture/écriture, cette méthode échoue. Bien que cette méthode puisse être utilisée avec les magasins de mémoire, toute modification apportée à un magasin de mémoire n’est pas conservée lors de la fermeture de la Banque.

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
</dt> </dl>

 

 
