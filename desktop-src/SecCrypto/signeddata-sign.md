---
description: Crée une signature numérique sur le contenu à signer. Une signature numérique se compose d’un hachage du contenu à signer qui est chiffré à l’aide de la clé privée du signataire.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: SignedData. Sign, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6ead7fb1c96b05d6945bb67937b215fd6d5d2422041250bee18e4be26edb2f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899017"
---
# <a name="signeddatasign-method"></a>SignedData. Sign, méthode

\[La méthode **Sign** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Sign** crée une [*signature numérique*](../secgloss/d-gly.md) sur le contenu à signer. Une signature numérique se compose d’un [*hachage*](../secgloss/h-gly.md) du contenu à signer qui est chiffré à l’aide de la clé privée du signataire. Cette méthode ne peut être utilisée qu’une fois que la propriété [**SignedData. Content**](signeddata-content.md) a été initialisée. Si la méthode **Sign** est appelée sur un objet qui a déjà une signature, l’ancienne signature est remplacée. La signature est créée à l’aide de l’algorithme de signature SHA1.

## <a name="syntax"></a>Syntaxe


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Signataire* \[ dans, facultatif\]
</dt> <dd>

Référence à l’objet [**signataire**](signer.md) du signataire des données. L’objet **signataire** doit avoir accès à la [*clé privée*](../secgloss/p-gly.md) du [*certificat*](../secgloss/c-gly.md) utilisé pour la signature. Ce paramètre peut avoir la **valeur null**; Pour plus d’informations, consultez la section Notes.

</dd> <dt>

*bDetached* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, les données à signer sont détachées ; autrement dit, le contenu signé n’est pas inclus dans l’objet signé. Pour vérifier la signature sur du contenu détaché, une application doit avoir une copie du contenu d’origine. Le contenu détaché est souvent utilisé pour réduire la taille d’un objet signé à envoyer sur le Web, si le destinataire du message signé contient une copie originale des données signées. La valeur par défaut est **False**.

</dd> <dt>

*EncodingType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [ \_ \_ type d’encodage](capicom-encoding-type.md) CAPICOM qui indique comment les données signées doivent être encodées. La valeur par défaut est CAPICOM \_ encode \_ Base64. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                  | Signification                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**\_coder \_ tout**</dt> </dl>          | Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu. Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place. Introduit dans CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Encode \_ Base64**</dt> </dl> | Les données sont enregistrées sous la forme d’une chaîne encodée en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt> </dl> | Les données sont enregistrées sous la forme d’une séquence binaire pure.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une chaîne qui contient les données signées et encodées.

Si cette méthode échoue, une erreur est levée. L’objet **Err** contient des informations supplémentaires sur l’erreur.

## <a name="remarks"></a>Remarques

> [!IMPORTANT]
> Lorsque cette méthode est appelée à partir d’un script Web, le script doit utiliser votre clé privée pour créer une signature numérique. Autoriser les sites Web non approuvés à utiliser votre clé privée est un risque pour la sécurité. Une boîte de dialogue qui vous demande si le site Web peut utiliser votre clé privée s’affiche lorsque cette méthode est appelée pour la première fois. Si vous autorisez le script à utiliser votre clé privée pour créer une signature numérique et que vous sélectionnez ne plus afficher cette boîte de dialogue, la boîte de dialogue n’apparaît plus pour les scripts de ce domaine qui utilisent votre clé privée pour créer une signature numérique. Toutefois, les scripts en dehors de ce domaine qui tentent d’utiliser votre clé privée pour créer une signature numérique entraînent toujours l’affichage de cette boîte de dialogue. Si vous n’autorisez pas le script à utiliser votre clé privée et que vous sélectionnez ne plus afficher cette boîte de dialogue, les scripts de ce domaine se verront automatiquement refuser la possibilité d’utiliser votre clé privée pour créer des signatures numériques.

 

Étant donné que la création d’une [*signature numérique*](../secgloss/d-gly.md) requiert l’utilisation d’une [*clé privée*](../secgloss/p-gly.md), les applications Web qui essaient d’utiliser cette méthode nécessitent des invites d’interface utilisateur qui permettent à l’utilisateur d’approuver l’utilisation de la clé privée, pour des raisons de sécurité.

Les résultats suivants s’appliquent à la valeur du paramètre de *signataire* :

-   Si le paramètre de *signataire* n’a pas la **valeur null**, cette méthode utilise la clé privée désignée par le certificat associé pour chiffrer la signature. Si la clé privée vers laquelle pointe le certificat n’est pas disponible, la méthode échoue.
-   Si le paramètre de *signataire* a la **valeur null** et qu’il y a exactement un certificat dans l' \_ utilisateur actuel mon magasin qui a accès à une clé privée, ce certificat est utilisé pour créer la signature.
-   si le paramètre de *signataire* a la **valeur NULL**, le [**Paramètres.**](settings-enablepromptforcertificateui.md)La valeur de la propriété EnablePromptForCertificateUI est true et il existe plusieurs certificats dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible, une boîte de dialogue s’affiche et permet à l’utilisateur de sélectionner le certificat à utiliser.
-   si le paramètre de *signataire* a la **valeur NULL** et que le [**Paramètres.**](settings-enablepromptforcertificateui.md)La propriété EnablePromptForCertificateUI a la valeur false, la méthode échoue.
-   Si le paramètre de *signataire* a la **valeur null** et qu’il n’existe aucun certificat dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible, la méthode échoue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
