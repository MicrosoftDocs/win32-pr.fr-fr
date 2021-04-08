---
description: CryptXML permet aux développeurs d’étendre les algorithmes de chiffrement pris en charge en mode natif en inscrivant une DLL d’extension de chiffrement à l’ensemble du système.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensions de chiffrement de signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869329"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Extensions de chiffrement de signature numérique XML

CryptXML permet aux développeurs d’étendre les algorithmes de chiffrement pris en charge en mode natif en inscrivant une DLL d’extension de chiffrement à l’ensemble du système. Les dll d’extension étendent les algorithmes pris en charge par les éléments XML **SignatureMethod** et **DigestMethod** . Les dll d’extension peuvent prendre en charge des algorithmes qui encodent des paramètres supplémentaires dans la signature numérique XML.

Toutes les dll d’extension doivent prendre en charge la fonction [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , qui retourne un pointeur vers une structure d' [**\_ \_ \_ interface de chiffrement XML énigmatique**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) . Cette structure fournit des pointeurs de fonction vers les fonctions d’extension de chiffrement implémentées. Les fonctions prises en charge dépendent du type d’algorithme de chiffrement pris en charge et de la nécessité de coder les paramètres dans la signature numérique XML.

Les fonctions d’extensions de chiffrement incluent les pointeurs de fonction suivants :

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Fonctions requises
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Fonctions de méthode Digest
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Fonctions de méthode de signature
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Pour les algorithmes avec des paramètres encodés par défaut
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Les dll d’extension de chiffrement sont inscrites à l’échelle du système. Des privilèges d’administrateur sont nécessaires pour inscrire une DLL d’extension de chiffrement.

Toutes les extensions de chiffrement CryptXML sont inscrites par la valeur d’URI définie dans le champ **SignatureMethod** ou attribut d’algorithme de l’élément **DigestMethod** .

Les chemins d’accès au registre des dll d’extension sont les suivants :

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32 bits
</dt> <dd>

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bits
</dt> <dd>

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> </dl>

Chaque clé contient les paramètres suivants.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Données</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DLL<br/></td>
<td>Chaîne extensible<br/></td>
<td>Obligatoire.<br/>Chemin d’accès absolu à la DLL du fournisseur de services de chiffrement XML.
<blockquote>
<p><b>Remarque : </b> Nous vous recommandons de placer les dll d’extension de chiffrement dans les répertoires qui peuvent uniquement être écrits par les applications avec des privilèges d’administrateur.</p>
<p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> est utilisé pour charger la dll d’extension de chiffrement.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Nom<br/></td>
<td><strong>Chaîne</strong></td>
<td>Optionnel.<br/> Nom complet associé à cet URI.<br/></td>
</tr>
<tr class="odd">
<td>GroupId<br/></td>
<td><strong>GRANDE</strong></td>
<td>Obligatoire.<br/> Identificateur de groupe associé à cet algorithme de chiffrement. Les valeurs possibles sont les suivantes :<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1<br/><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2<br/></td>
</tr>
<tr class="even">
<td>CNGAlgid<br/></td>
<td><strong>Chaîne</strong></td>
<td>Obligatoire.<br/> Nom de l’algorithme CNG à transmettre aux fonctions BCrypt ou NCrypt.<br/></td>
</tr>
<tr class="odd">
<td>CNGExtraAlgid<br/></td>
<td><strong>Chaîne</strong></td>
<td>Optionnel.<br/> Chaîne d’algorithme supplémentaire, autre que la chaîne du membre CNGAlgid, qui peut être passée aux fonctions CNG.<br/> Pour les algorithmes de signature (CRYPT_XML_GROUP_ID_SIGN), ce membre est la chaîne de l’algorithme de clé publique à passer aux fonctions CNG.<br/> Pour les autres valeurs de GroupId, définissez le membre <strong>pwszCNGExtraAlgid</strong> sur la chaîne vide, L &quot; &quot; . <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>


</dt> <dt>

[Algorithmes de chiffrement de signature numérique XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
