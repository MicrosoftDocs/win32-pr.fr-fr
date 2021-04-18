---
description: Spécifie un certificat de signature (également connu sous le nom de certificat de l’agent d’inscription).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'ISCrdEnr :: setSigningCertificate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522828"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>ISCrdEnr :: setSigningCertificate, méthode

La méthode **setSigningCertificate** spécifie un certificat de signature (également appelé *certificat* de l’agent d’inscription).

Avant de procéder à l’inscription au nom des utilisateurs, vous devez sélectionner ou définir un certificat de signature. La [*clé privée*](../secgloss/p-gly.md) associée à ce certificat de signature est utilisée pour signer une \# demande PKCS 7. Le PKCS \# 7, quant à lui, contient la requête PKCS 10 de l’utilisateur \# (qui est signée avec la clé privée de l’utilisateur).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé pour un usage futur. Définissez cette valeur sur zéro.

</dd> <dt>

*bstrCertTemplateName* \[ dans\]
</dt> <dd>

Nom du modèle de certificat pour le certificat de signature. Vous pouvez utiliser la valeur « EnrollmentAgent » si vous avez obtenu un certificat EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="vb"></a>VB

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Notes

Avant de procéder à l’inscription pour le compte d’un utilisateur, vous devez d’abord obtenir un certificat de signature. Vous pouvez obtenir un certificat de signature à l’aide du composant logiciel enfichable MMC du gestionnaire de certificats. La méthode **setSigningCertificate** n’obtient pas le certificat de signature, mais informe le contrôle d’inscription de carte à puce qui a précédemment obtenu le certificat de signature à utiliser. La méthode **setSigningCertificate** recherche le certificat de signature le plus récent correspondant au modèle de certificat spécifié par *bstrCertTemplateName* dans le magasin My de l’appelant.

Une alternative à **setSigningCertificate** est **ISCrdEnr :: setSigningCertificate**.

Une fois le certificat de signature défini, son nom peut être récupéré en appelant [**ISCrdEnr :: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
