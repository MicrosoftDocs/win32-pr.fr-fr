---
description: Retourne un objet BasicConstraints qui représente l’extension de contraintes de base du certificat.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'ICertificate2 :: BasicConstraints, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8958a942a8c56dfe39c8a96bcf3f80cefcb7978feac186a80432cbe8f03b5c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127149"
---
# <a name="icertificate2basicconstraints-method"></a>ICertificate2 :: BasicConstraints, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **basicConstraints** retourne un objet [**basicConstraints**](basicconstraints.md) qui représente l’extension de contraintes de base du certificat.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Objet [**basicConstraints**](basicconstraints.md) qui représente l’extension de contraintes de base du certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
