---
description: Utilisé avec les fonctions BCryptGetProperty et BCryptSetProperty pour identifier une propriété.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificateurs de propriété primitifs de chiffrement (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861970"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificateurs de la propriété primitive de chiffrement

Les valeurs suivantes sont utilisées avec les fonctions [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) et [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) pour identifier une propriété.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**nom de l' \_ algorithme BCRYPT \_**
</dt> <dd> <dl> <dt>

L « AlgorithmName »
</dt> <dt>



Chaîne Unicode terminée par le caractère null qui contient le nom de l’algorithme.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**longueur de la \_ balise d’authentification BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L « AuthTagLength »
</dt> <dt>



Les longueurs d’étiquette d’authentification prises en charge par l’algorithme. Cette propriété est une structure de structure de [**\_ \_ \_ longueurs \_ d’authentification BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Cette propriété s’applique uniquement aux algorithmes.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_longueur du bloc BCRYPT \_**
</dt> <dd> <dl> <dt>

L « BlockLength »
</dt> <dt>



Taille, en octets, d’un bloc de chiffrement pour l’algorithme. Cette propriété s’applique uniquement aux algorithmes de chiffrement par bloc. Ce type de données est un **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_liste des \_ tailles de bloc BCRYPT \_**
</dt> <dd> <dl> <dt>

L « BlockSizeList »
</dt> <dt>



Liste des longueurs de bloc prises en charge par un algorithme de chiffrement. Ce type de données est un tableau de **DWORDS**. Le nombre d’éléments dans le tableau peut être déterminé en divisant le nombre d’octets récupérés par la taille d’une **valeur DWORD** unique.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_mode de chaînage \_ BCRYPT**
</dt> <dd> <dl> <dt>

L « ChainingMode »
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui représente le mode de chaînage de l’algorithme de chiffrement. Cette propriété peut être définie sur un handle d’algorithme ou un handle de clé sur l’une des valeurs suivantes.



| Identificateur                   | Valeur                         | Description                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_mode chaîne \_ BCRYPT \_ CBC** | L « ChainingModeCBC »<br/> | Définit le mode de chaînage de l’algorithme pour [*chiffrer les chaînages de blocs*](/windows/desktop/SecGloss/c-gly).<br/>            |
| **\_ \_ CCM en mode \_ chaîné** | L « ChainingModeCCM »<br/> | Définit le mode de chaînage de l’algorithme sur compteur avec le mode CBC-MAC (CCM). **Windows Vista :** Cette valeur est prise en charge à partir de Windows Vista avec SP1.<br/> <br/> |
| **\_mode de chaîne BCRYPT \_ \_ CFB** | L « ChainingModeCFB »<br/> | Définit le mode de chaînage de l’algorithme pour [*chiffrer les commentaires*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **\_ \_ BCE en mode de chaîne BCRYPT \_** | L « ChainingModeECB »<br/> | Définit le mode de chaînage de l’algorithme sur [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).<br/>                  |
| **\_mode de chaîne BCRYPT \_ \_ GCM** | L « ChainingModeGCM »<br/> | Définit le mode de chaînage de l’algorithme en mode Galois/Counter (GCM). **Windows Vista :** Cette valeur est prise en charge à partir de Windows Vista avec SP1.<br/> <br/>       |
| **\_mode de chaîne BCRYPT \_ \_ na**  | L "ChainingModeN/A"<br/> | L’algorithme ne prend pas en charge le chaînage.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_paramètres BCRYPT DH \_**
</dt> <dd> <dl> <dt>

L « DHParameters »
</dt> <dt>



Spécifie les paramètres à utiliser avec une clé de Diffie-Hellman. Ce type de données est un pointeur vers une structure d' [**\_ \_ \_ en-tête de paramètre BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Cette propriété peut uniquement être définie et doit être définie pour la clé avant la fin de la clé.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_paramètres du DSA de BCRYPT \_**
</dt> <dd> <dl> <dt>

L « DSAParameters »
</dt> <dt>



Spécifie les paramètres à utiliser avec une clé DSA. Cette propriété est un [**\_ \_ \_ en-tête de paramètre DSA DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) ou une structure d' [**\_ \_ \_ en-tête \_ de paramètre DSA DSA v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Cette propriété peut uniquement être définie et doit être définie pour la clé avant la fin de la clé.

**Windows 8 :** À partir de Windows 8, cette propriété peut être une structure d' [**\_ \_ \_ en \_ -tête de paramètre DSA DSA v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Utilisez cette structure si la taille de la clé dépasse 1024 bits et est inférieure ou égale à 3072 bits. Si la taille de la clé est supérieure ou égale à 512, mais inférieure ou égale à 1024 bits, utilisez la structure d' [**\_ \_ \_ en-tête de paramètre DSA DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_longueur de \_ clé en vigueur BCRYPT \_**
</dt> <dd> <dl> <dt>

L « EffectiveKeyLength »
</dt> <dt>



Taille, en bits, de la longueur effective d’une clé RC2. Ce type de données est un **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_longueur du \_ bloc de hachage BCRYPT \_**
</dt> <dd> <dl> <dt>

L « HashBlockLength »
</dt> <dt>



Taille, en octets, du bloc pour un hachage. Cette propriété s’applique uniquement aux algorithmes de hachage. Ce type de données est un **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_longueur de hachage BCRYPT \_**
</dt> <dd> <dl> <dt>

L « HashDigestLength »
</dt> <dt>



Taille, en octets, de la valeur de hachage d’un fournisseur de hachage. Ce type de données est un **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_liste d' \_ OID de hachage BCRYPT \_**
</dt> <dd> <dl> <dt>

L « HashOIDList »
</dt> <dt>



Liste des [*identificateurs d’objet*](/windows/desktop/SecGloss/o-gly) (OID) de hachage codé [*der*](/windows/desktop/SecGloss/d-gly). Cette propriété est une structure de [**\_ \_ liste d’OID BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) . Cette propriété peut uniquement être lue.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_vecteur d’initialisation de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



Contient le [*vecteur d’initialisation*](/windows/desktop/SecGloss/i-gly) (IV) pour une clé. Cette propriété s’applique uniquement aux clés.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_longueur de clé BCRYPT \_**
</dt> <dd> <dl> <dt>

L "keylength"
</dt> <dt>



Taille, en bits, de la valeur de clé d’un fournisseur de clé symétrique. Ce type de données est un **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_longueurs de clé BCRYPT \_**
</dt> <dd> <dl> <dt>

L "caractères de longueur"
</dt> <dt>



Longueurs de clé prises en charge par l’algorithme. Cette propriété est une structure de structure de [**\_ \_ longueurs \_ de clé BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Cette propriété s’applique uniquement aux algorithmes.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**longueur de l' \_ objet de clé BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L « KeyObjectLength »
</dt> <dt>



Cette propriété n'est pas utilisée. La **propriété \_ \_ longueur de l’objet BCRYPT** est utilisée pour obtenir ces informations.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_puissance de clé BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyForce"
</dt> <dt>



Nombre de bits dans la clé. Ce type de données est un **DWORD**. Cette propriété s’applique uniquement aux clés.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_longueur du \_ bloc de message BCRYPT \_**
</dt> <dd> <dl> <dt>

L « MessageBlockLength »
</dt> <dt>



Cela peut être défini sur n’importe quel handle de clé pour lequel le mode de chaînage de CFB est défini. Par défaut, cette propriété a la valeur 1 pour le CFB 8 bits. Si vous définissez cette valeur sur la taille de bloc en octets, vous pouvez utiliser le mode CFB de bloc complet. Pour les clés XTS, il est utilisé pour définir la taille, en octets, de l’unité de données XTS (généralement 512 ou 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_longueur de plusieurs \_ objets \_ BCRYPT**
</dt> <dd> <dl> <dt>

L « MultiObjectLength »
</dt> <dt>



Cette propriété retourne un [**\_ struct de \_ \_ longueur d' \_ objet multiple de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), qui contient les informations nécessaires pour calculer la taille d’une mémoire tampon d’objet. Cette propriété est uniquement prise en charge sur les versions de système d’exploitation qui prennent en charge la fonction [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**longueur de l' \_ objet BCRYPT \_**
</dt> <dd> <dl> <dt>

L « ObjectLength »
</dt> <dt>



Taille, en octets, du sous-objet d’un fournisseur. Ce type de données est un **DWORD**. Actuellement, les fournisseurs d’algorithmes de chiffrement et de hachage symétrique utilisent des mémoires tampons allouées par l’appelant pour stocker leurs sous-objets. Par exemple, le fournisseur de hachage vous oblige à allouer de la mémoire pour l’objet de hachage obtenu avec la fonction [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Cette propriété fournit la taille de la mémoire tampon pour l’objet d’un fournisseur afin que vous puissiez allouer de la mémoire pour l’objet créé par le fournisseur.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_schémas de remplissage \_ BCRYPT**
</dt> <dd> <dl> <dt>

L « PaddingSchemes »
</dt> <dt>



Représente le schéma de remplissage du fournisseur de l’algorithme RSA. Ce type de données est un **DWORD**. Il peut s’agir de l’une des valeurs suivantes.



| Identificateur                             | Valeur      | Description                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **\_routeur de \_ Pad pris en charge par BCRYPT \_**     | 0x00000001 | Le fournisseur prend en charge le remplissage ajouté par le routeur.         |
| **BCRYPT \_ Pad pris en charge \_ \_ PKCS1 \_ enc** | 0x00000002 | Le fournisseur prend en charge le schéma de remplissage de chiffrement PKCS1. |
| **BCRYPT \_ Supported \_ Pad \_ PKCS1 \_ SIG** | 0x00000004 | Le fournisseur prend en charge le schéma de remplissage de signature PKCS1.  |
| **BCRYPT \_ Pad pris en charge par BCRYPT \_ \_**       | 0x00000008 | Le fournisseur prend en charge le schéma de remplissage OAEP.             |
| **\_ \_ support technique de tapis pris en charge par BCRYPT \_**        | 0x00000010 | Le fournisseur prend en charge le schéma de remplissage PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_handle du fournisseur BCRYPT \_**
</dt> <dd> <dl> <dt>

L « ProviderHandle »
</dt> <dt>



Handle du fournisseur CNG qui a créé l’objet passé dans le paramètre *hObject* . Ce type de données est **une \_ \_ poignée de BCRYPT ALG**. Cette propriété peut uniquement être récupérée. elle ne peut pas être définie.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**longueur de la \_ signature BCRYPT \_**
</dt> <dd> <dl> <dt>

L « SignatureLength »
</dt> <dt>



Taille, en octets, de la longueur d’une signature pour une clé. Ce type de données est un **DWORD**. Cette propriété s’applique uniquement aux clés. Cette propriété peut uniquement être récupérée. elle ne peut pas être définie.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



 

