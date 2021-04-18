---
description: Crée une signature numérique sur le contenu précédemment signé.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. cosign, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533465"
---
# <a name="signeddatacosign-method"></a>SignedData. cosign, méthode

\[La méthode de **cosignature** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **cosign** crée une [*signature numérique*](../secgloss/d-gly.md) sur le contenu précédemment signé.

## <a name="syntax"></a>Syntaxe


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Signataire* \[ dans, facultatif\]
</dt> <dd>

Référence à l’objet [**signataire**](signer.md) du signataire des données. L’objet **signataire** doit avoir accès à la clé privée du certificat utilisé pour la signature. Ce paramètre peut avoir la **valeur null**; Pour plus d’informations, consultez la section Notes.

</dd> <dt>

*EncodingType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique comment les données signées doivent être encodées. La valeur par défaut est CAPICOM \_ encode \_ Base64. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                  | Signification                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**\_coder \_ tout**</dt> </dl>          | Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu. Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place. Introduit dans CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Encode \_ Base64**</dt> </dl> | Les données sont enregistrées sous la forme d’une chaîne encodée en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt> </dl> | Les données sont enregistrées sous la forme d’une séquence binaire pure.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une chaîne qui contient les données signées et encodées.

Si cette méthode échoue, une erreur est levée. L’objet **Err** contient des informations supplémentaires sur l’erreur.

## <a name="remarks"></a>Notes

> [!IMPORTANT]
> Lorsque cette méthode est appelée à partir d’un script Web, le script doit utiliser votre [*clé privée*](../secgloss/p-gly.md) pour créer une signature numérique. Autoriser les sites Web non approuvés à utiliser votre clé privée est un risque pour la sécurité. Une boîte de dialogue qui vous demande si le site Web peut utiliser votre clé privée s’affiche lorsque cette méthode est appelée pour la première fois. Si vous autorisez le script à utiliser votre clé privée pour créer une signature numérique et que vous sélectionnez ne plus afficher cette boîte de dialogue, la boîte de dialogue n’apparaît plus pour les scripts de ce domaine qui utilisent votre clé privée pour créer une signature numérique. Toutefois, les scripts en dehors de ce domaine qui tentent d’utiliser votre clé privée pour créer une signature numérique entraînent toujours l’affichage de cette boîte de dialogue. Si vous n’autorisez pas le script à utiliser votre clé privée et que vous sélectionnez ne plus afficher cette boîte de dialogue, les scripts de ce domaine se verront automatiquement refuser la possibilité d’utiliser votre clé privée pour créer des signatures numériques.

 

Il n’est pas garanti que les cosignataires soient dans un ordre particulier.

Les résultats suivants s’appliquent à la valeur du paramètre de *signataire* :

-   Si le paramètre de *signataire* n’a pas la **valeur null**, cette méthode utilise la clé privée désignée par le certificat associé pour chiffrer la cosignature. Si la clé privée vers laquelle pointe le certificat n’est pas disponible, la méthode échoue.
-   Si le paramètre de *signataire* a la **valeur null** et qu’il y a exactement un certificat dans l' \_ utilisateur actuel mon magasin qui a accès à une clé privée, ce certificat est utilisé pour créer la cosignature.
-   Si le paramètre du *signataire* a la valeur **null**, la valeur de la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) est true et qu’il y a plusieurs certificats dans le magasin de l' \_ utilisateur actuel mon magasin avec une clé privée disponible, une boîte de dialogue s’affiche et permet à l’utilisateur de sélectionner le certificat à utiliser.
-   Si le paramètre de *signataire* a la **valeur null** et que la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) a la valeur false, la méthode échoue.
-   Si le paramètre de *signataire* a la **valeur null** et qu’il n’existe aucun certificat dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible, la méthode échoue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
