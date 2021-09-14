---
description: Affiche une boîte de dialogue permettant de sélectionner des certificats et retourne une collection de ces certificats sélectionnés.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'ICertificates2 :: Select, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237702"
---
# <a name="icertificates2select-method"></a>ICertificates2 :: Select, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Select** affiche une boîte de dialogue permettant de sélectionner des certificats et renvoie une collection des certificats sélectionnés. Cette méthode a été introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Titre* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le titre de la boîte de dialogue. La valeur par défaut est une chaîne vide ("").

</dd> <dt>

*DisplayString* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le texte d’invite affiché avec la boîte de dialogue. La valeur par défaut est une chaîne vide ("").

</dd> <dt>

*bMultiSelect* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si l’utilisateur peut sélectionner plusieurs certificats. True indique qu’il est possible de sélectionner plusieurs certificats à l’aide de la touche CTRL ou Maj. La valeur par défaut est false.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Objet de [**certificats**](certificates.md) qui contient les certificats sélectionnés dans la boîte de dialogue.

**Capicom 2,1 :** L’objet de [**certificats**](certificates.md) retourné contient des références aux certificats de la collection à partir de laquelle la sélection a été effectuée. Toutes les modifications apportées aux certificats de l’objet **certificats** retournés sont répercutées dans cette collection.

**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 et ca-2.0.0.3** de la façon suivante : L’objet de [**certificats**](certificates.md) retourné contient des copies des certificats dans la collection à partir de laquelle la sélection a été effectuée. Les modifications apportées aux certificats de l’objet **certificats** retournés ne sont pas reflétées dans cette collection.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
