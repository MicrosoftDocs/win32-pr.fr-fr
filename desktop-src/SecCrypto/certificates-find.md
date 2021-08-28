---
description: Retourne un objet de certificats qui contient tous les certificats qui correspondent aux critères de recherche spécifiés.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: 'ICertificates2 :: Find, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100989"
---
# <a name="icertificates2find-method"></a>ICertificates2 :: Find, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Find** retourne un objet [**Certificates**](certificates.md) qui contient tous les certificats qui correspondent aux critères de recherche spécifiés. Cette méthode a été introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FindType* \[ dans\]
</dt> <dd>

La valeur du [**\_ certificat CAPICOM \_ trouve \_**](capicom-certificate-find-type.md) l’énumération de type qui spécifie le type de critères de correspondance fourni dans le paramètre *varCriteria* . Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                                        | Signification                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**Le certificat CAPICOM \_ \_ trouve un \_ \_ hachage SHA1**</dt> </dl>                              | Retourne les certificats avec un hachage SHA1 qui correspond au hachage SHA1 spécifié dans le paramètre *varCriteria* .<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**le certificat CAPICOM \_ trouve le nom de l' \_ \_ objet \_**</dt> </dl>                     | Retourne les certificats dont le nom de sujet correspond exactement ou partiellement au nom d’objet spécifié dans le paramètre *varCriteria* . Cet appel recherche uniquement dans le champ nom de l’objet.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**le certificat CAPICOM \_ trouve le nom de l' \_ \_ émetteur \_**</dt> </dl>                        | Retourne les certificats dont le nom de l’émetteur correspond exactement ou partiellement au nom de l’émetteur spécifié dans le paramètre *varCriteria* . Cet appel recherche uniquement le champ du nom de l’émetteur.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**\_ \_ \_ nom racine de la recherche du certificat CAPICOM \_**</dt> </dl>                              | Retourne les certificats dont le nom d’objet racine correspond exactement ou partiellement au nom d’objet racine spécifié dans le paramètre *varCriteria* . Cet appel crée une chaîne. Cet appel recherche dans le champ nom de l’objet du certificat racine.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**\_nom du modèle de \_ recherche de certificat \_ CAPICOM \_**</dt> </dl>                  | Retourne les certificats dont le nom de modèle correspond au nom de modèle spécifié dans le paramètre *varCriteria* .<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**EXTENSION de recherche de \_ certificat CAPICOM \_ \_**</dt> </dl>                               | Retourne les certificats qui ont une extension qui correspond à l’extension spécifiée dans le paramètre *varCriteria* .<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**la \_ \_ \_ \_ propriété étendue de la recherche du certificat CAPICOM**</dt> </dl>      | Retourne des certificats dans le magasin qui contiennent explicitement une propriété étendue avec la valeur spécifiée dans le paramètre *varCriteria* .<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**certificat CAPICOM- \_ \_ stratégie d' \_ application de recherche \_**</dt> </dl>   | Retourne les certificats dans le magasin qui ont une extension d’utilisation de clé améliorée, une extension de stratégie d’application ou une propriété étendue spécifiée dans le paramètre *varCriteria* .<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**certificat CAPICOM- \_ \_ Rechercher la \_ stratégie de certificat \_**</dt> </dl>   | Retourne les certificats qui contiennent l’OID de stratégie dans l’extension de stratégie de certificat spécifiée dans le paramètre *varCriteria* .<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**\_temps de recherche du certificat CAPICOM \_ \_ \_ valide**</dt> </dl>                           | Retourne les certificats dont l’heure est valide.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**l’heure de la \_ recherche du certificat CAPICOM n’est \_ \_ \_ pas \_ encore \_ valide**</dt> </dl> | Retourne des certificats dont l’heure n’est pas encore valide.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**\_temps de recherche du certificat CAPICOM \_ \_ \_ expiré**</dt> </dl>                     | Retourne les certificats dont le temps a expiré.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**utilisation de la \_ \_ clé de recherche de certificat CAPICOM \_ \_**</dt> </dl>                              | Retourne les certificats contenant des utilisations de clés dans l’extension KeyUsage spécifiée dans le paramètre *varCriteria* . Si l’extension KeyUsage n’est pas présente, il est supposé que toutes les utilisations de la clé ne sont pas disponibles.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ dans, facultatif\]
</dt> <dd>

Variante qui contient les critères de recherche. Ces données doivent correspondre au type de données spécifié dans le paramètre *FindType* . Si la valeur du paramètre *FindType* est l’heure de la \_ recherche du certificat CAPICOM \_ \_ \_ valide, que le \_ certificat \_ CAPICOM \_ \_ n’est pas \_ encore \_ valide ou \_ que le certificat CAPICOM a \_ \_ \_ expiré et que vous ne transmettez pas de valeur dans ce paramètre, l’heure actuelle est utilisée. Pour obtenir des exemples de chaque type de données, consultez la section Notes. La valeur par défaut est 0.

</dd> <dt>

*bFindValidOnly* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si seuls les certificats valides sont retournés. La valeur par défaut est false. Cela indique que tous les certificats qui correspondent aux critères de recherche sont retournés.

Si la valeur est true, la recherche ne retourne pas les types de certificats suivants :

-   Certificats dont l’heure a expiré ou qui n’est pas encore valide.
-   Certificats non chaînés correctement.
-   Certificats qui présentent des problèmes de signature.
-   Certificats révoqués.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet de [**certificats**](certificates.md) qui contient les résultats de la recherche.

**Capicom 2,1 :** L’objet de [**certificats**](certificates.md) retourné contient des références aux certificats de la collection dans laquelle la recherche a été effectuée. Toutes les modifications apportées aux certificats de l’objet **certificats** retournés sont répercutées dans cette collection.

**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 et ca-2.0.0.3** de la façon suivante : L’objet de [**certificats**](certificates.md) retourné contient des copies des certificats de la collection dans laquelle la recherche a été effectuée. Les modifications apportées aux certificats de l’objet **certificats** retournés ne sont pas reflétées dans cette collection.

## <a name="remarks"></a>Remarques

Les exemples suivants illustrent les critères de recherche possibles pour les différents types de critères de recherche.



| Paramètre *FindType*                              | paramètre *varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Le certificat CAPICOM \_ \_ trouve un \_ \_ hachage SHA1            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| le certificat CAPICOM \_ trouve le nom de l' \_ \_ objet \_         | "NameOfPerson"                                                                                                                     |
| le certificat CAPICOM \_ trouve le nom de l' \_ \_ émetteur \_          | VeriSign                                                                                                                         |
| \_ \_ \_ nom racine de la recherche du certificat CAPICOM \_            | « Autorité racine Microsoft »                                                                                                         |
| \_nom du modèle de \_ recherche de certificat \_ CAPICOM \_        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| EXTENSION de recherche de \_ certificat CAPICOM \_ \_             | "2.5.29.31"<br/> EXTENSION d’utilisation de la \_ clé CAPICOM OID \_ \_ \_<br/> « Liste de distribution de liste de révocation des certificats »<br/>                           |
| la \_ \_ \_ \_ propriété étendue de la recherche du certificat CAPICOM    | CAPICOM- \_ \_ \_ informations sur la clé \_ de l’ID de la clé                                                                                                   |
| certificat CAPICOM- \_ \_ stratégie d' \_ application de recherche \_   | 1.3.6.1.5.5.7.3.3<br/> 1.3.6.1.5.5.7.3.4<br/> \_ \_ \_ authentification EKU du serveur CAPICOM OID \_<br/> « Signature du code »<br/> |
| certificat CAPICOM- \_ \_ Rechercher la \_ stratégie de certificat \_   | "1.3.6.1.5.5.7.3.4.3.5"<br/> « Assurance élevée de l’entreprise »<br/>                                                           |
| \_temps de recherche du certificat CAPICOM \_ \_ \_ valide           | \#04/15/2002, 6:00 H 00\#                                                                                                            |
| l’heure de la \_ recherche du certificat CAPICOM n’est \_ \_ \_ pas \_ encore \_ valide | \#04/15/2002, 6:00 H 00\#                                                                                                            |
| \_temps de recherche du certificat CAPICOM \_ \_ \_ expiré         | \#04/15/2002, 6:00 H 00\#                                                                                                            |
| utilisation de la \_ \_ clé de recherche de certificat CAPICOM \_ \_            | utilisation de la \_ clé d’ENchiffrement CAPICOM \_ uniquement \_ \_                                                                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Certificats**](certificates.md)
</dt> <dt>

[**\_OID CAPICOM**](capicom-oid.md)
</dt> </dl>

 

 
