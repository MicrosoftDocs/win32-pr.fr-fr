---
description: Déchiffre le contenu enveloppé.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData. Decrypt, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f1c754e23977ac9c7af7f4fd3feaade13c928e9522a2285102a095fff4740b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874259"
---
# <a name="envelopeddatadecrypt-method"></a>EnvelopedData. Decrypt, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Decrypt** déchiffre le contenu enveloppé. Le déchiffrement s’effectue si le destinataire du message a accès à la [*clé privée*](../secgloss/p-gly.md) associée à l’une des [*clés publiques*](../secgloss/p-gly.md) utilisées pour encapsuler le message. L’appel de la méthode **Decrypt** réinitialise l' [*État*](../secgloss/s-gly.md) de l’objet. Si la méthode de **déchiffrement** est établie, la propriété [**contenu**](envelopeddata-content.md) de l’objet [**EnvelopedData**](envelopeddata.md) est définie sur le message de texte en clair.

## <a name="syntax"></a>Syntaxe


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EnvelopedMessage* \[ dans\]
</dt> <dd>

Chaîne qui contient les données enveloppées à déchiffrer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les données déchiffrées deviennent la valeur de la propriété de [**contenu**](envelopeddata-content.md) de l’objet [**EnvelopedData**](envelopeddata.md) .

Si l’utilisateur de cette méthode n’a pas accès à une clé privée qui correspond à l’une des clés publiques utilisées pour encapsuler le message, la méthode échoue. Cette méthode échoue si le certificat de la clé privée associée ne figure pas dans l’ordinateur local mon magasin ou dans le magasin de l’utilisateur actuel.

> [!IMPORTANT]
> Lorsque cette méthode est appelée à partir d’un script Web, le script doit utiliser votre [*clé privée*](../secgloss/p-gly.md) pour déchiffrer les données. Autoriser les sites Web non approuvés à utiliser votre clé privée est un risque pour la sécurité. Une boîte de dialogue qui vous demande si le site Web peut utiliser votre clé privée s’affiche lorsque cette méthode est appelée pour la première fois. Si vous autorisez le script à utiliser votre clé privée et que vous sélectionnez ne plus me le demander, la boîte de dialogue n’apparaît plus pour les scripts qui utilisent votre clé privée pour déchiffrer les données dans ce domaine. Toutefois, les scripts en dehors de ce domaine qui tentent d’utiliser votre clé privée pour déchiffrer des données entraînent l’affichage de cette boîte de dialogue. Si vous n’autorisez pas le script à utiliser votre clé privée et que vous sélectionnez ne plus me le demander, les scripts de ce domaine se verront automatiquement refuser la possibilité d’utiliser votre clé privée pour déchiffrer les données.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
