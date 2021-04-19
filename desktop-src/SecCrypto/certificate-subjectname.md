---
description: Récupère une chaîne qui contient le nom de l’objet du certificat.
ms.assetid: 95dc7e8b-6670-4dfc-9fe1-d37635fb92d6
title: Propriété Certificate. SubjectName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SubjectName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b17d99ab3ab485153a0af535aa74b9a9123ddaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545359"
---
# <a name="certificatesubjectname-property"></a>Propriété Certificate. SubjectName

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **SubjectName** récupère une chaîne qui contient le nom de l’objet du certificat.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.SubjectName As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le nom de l’objet du certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Certificat**](certificate.md)
</dt> </dl>

 

 
