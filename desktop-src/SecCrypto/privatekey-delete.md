---
description: Supprime le conteneur de clé privée référencé par l’objet PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542239"
---
# <a name="privatekeydelete-method"></a>PrivateKey. Delete, méthode

\[La méthode de **suppression** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Delete** supprime le conteneur de clé privée référencé par l’objet [**PrivateKey**](privatekey.md) .

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

> [!IMPORTANT]
> Cette méthode supprime le conteneur de clé privée référencé par l’objet [**PrivateKey**](privatekey.md) , ainsi que toutes les clés privées dans le conteneur. Tout ce qui est chiffré à l’aide des clés publiques correspondant aux clés privées supprimées ne pourra plus être déchiffré.

 

Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
