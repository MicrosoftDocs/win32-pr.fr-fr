---
description: Utilisé pour identifier une propriété de stockage de clé.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: identificateurs de propriété de clé Stockage (Ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b8fca27591837a555e4f75040ba16056c42e16ce488c0bb99f2d8f7de70bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907612"
---
# <a name="key-storage-property-identifiers"></a>identificateurs de propriété de clé Stockage

Les valeurs suivantes sont utilisées pour identifier une propriété de stockage de clé.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_propriété du groupe d’algorithmes NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "groupe d’algorithmes"
</dt> <dt>



Chaîne Unicode terminée par le caractère null qui contient le nom du groupe d’algorithmes de l’objet. Cette propriété s’applique uniquement aux clés. Les identificateurs suivants sont retournés par le fournisseur de stockage de clés Microsoft.



| Identificateur                                     | Valeur              | Description                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **\_groupe d' \_ algorithmes de RSA NCRYPT \_**<br/>   | DOTÉ<br/>   | Groupe d’algorithmes RSA.<br/>                           |
| **\_groupe d' \_ algorithmes de DH \_**<br/>    | VA<br/>    | Groupe d’algorithmes Diffie-Hellman.<br/>                |
| **\_groupe d' \_ algorithmes DSA NCRYPT \_**<br/>   | DSA<br/>   | Groupe d’algorithmes DSA.<br/>                           |
| **\_groupe d' \_ algorithmes ECDSA NCRYPT \_**<br/> | ECDsa<br/> | Groupe d’algorithmes DSA de la courbe elliptique.<br/>            |
| **\_groupe d' \_ algorithmes ECDH NCRYPT \_**<br/>  | ECDH<br/>  | Le groupe d’algorithmes Diffie-Hellman de courbe elliptique.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_propriété d’algorithme NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nom de l’algorithme"
</dt> <dt>



Chaîne Unicode terminée par le caractère null qui contient le nom de l’algorithme de l’objet. Il peut s’agir de l’un des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) prédéfinis ou d’un autre identificateur d’algorithme inscrit. Cette propriété s’applique uniquement aux clés.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_clé ECDH associée à NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L « SmartCardAssociatedECDHKey »
</dt> <dt>



Valeur **LPWStr** qui indique le nom de conteneur de la clé ECDH (elliptic Curve Diffie-Hellman) à utiliser lors de l’ouverture de session pour un handle donné à une clé ECDSA (Elliptic Curve Digital Signature Algorithm). S’il n’existe aucune clé ECDH sur la carte, le [*fournisseur de stockage de clés*](/windows/desktop/SecGloss/k-gly) (KSP) retourne le NPD est **\_ \_ introuvable**. Cette propriété s’applique aux clés ECDSA pour l’ouverture de session avec les cartes à puce. La propriété est prise en charge par le fournisseur de stockage de clés de carte à puce Microsoft et non par le fournisseur de stockage de clés logicielles Microsoft.

**Windows Server 2008 et Windows Vista :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_propriété de \_ longueur de bloc NCRYPT \_**
</dt> <dd> <dl> <dt>

L "longueur du bloc"
</dt> <dt>



**Valeur DWORD** qui contient la longueur, en octets, du bloc de chiffrement. Cette propriété s’applique uniquement aux clés qui prennent en charge le chiffrement.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_propriété du certificat NCRYPT \_**
</dt> <dd> <dl> <dt>

L « SmartCardKeyCertificate »
</dt> <dt>



[*Objet BLOB*](/windows/desktop/SecGloss/b-gly) qui contient un certificat X. 509 associé à la clé.

**Windows server 2008 R2, Windows 7, Windows Server 2008 et Windows Vista :** [*Objet BLOB*](/windows/desktop/SecGloss/b-gly) qui contient le [*certificat*](/windows/desktop/SecGloss/c-gly)de clé de [*carte à puce*](/windows/desktop/SecGloss/s-gly) . cette propriété n’est pas prise en charge par le fournisseur de Stockage de clés logicielles Microsoft.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**\_propriété des \_ paramètres NCRYPT DH \_**
</dt> <dd> <dl> <dt>

L « DHParameters »
</dt> <dt>



Spécifie les paramètres à utiliser avec une clé de Diffie-Hellman. Ce type de données est un pointeur vers une structure d' [**\_ \_ \_ en-tête de paramètre BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Cette propriété peut uniquement être définie et doit être définie pour la clé avant la fin de la clé.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**propriété de la \_ stratégie d’exportation NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L « stratégie d’exportation »
</dt> <dt>



Valeur **DWORD** qui contient un jeu d’indicateurs qui spécifient la stratégie d’exportation pour une clé rendue persistante. Cette propriété s’applique uniquement aux clés. Il peut contenir zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.



| Identificateur                                    | Valeur      | Description                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NCRYPT- \_ autoriser l' \_ indicateur d’exportation \_**               | 0x00000001 | La clé privée peut être exportée.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ autoriser \_ l' \_ indicateur d’exportation en texte clair \_**    | 0x00000002 | La clé privée peut être exportée sous forme de texte en clair.                                                                                                                                                                                                                                                               |
| **\_ \_ l’indicateur d’archivage d’autorisation NCRYPT \_**            | 0x00000004 | La clé privée peut être exportée une fois à des fins d’archivage. Cet indicateur s’applique uniquement au handle de clé d’origine sur lequel il est défini. Cette stratégie ne peut être appliquée qu’au handle de clé d’origine. Une fois le descripteur de clé fermé, la clé ne peut plus être exportée à des fins d’archivage.                   |
| **NCRYPT \_ autoriser \_ \_ l’indicateur d’archivage en texte clair \_** | 0x00000008 | La clé privée peut être exportée une seule fois sous forme de texte en clair à des fins d’archivage. Cet indicateur s’applique uniquement au handle de clé d’origine sur lequel il est défini. Cette stratégie ne peut être appliquée qu’au handle de clé d’origine. Une fois le descripteur de clé fermé, la clé ne peut plus être exportée à des fins d’archivage. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_propriété de \_ type impl impl \_**
</dt> <dd> <dl> <dt>

L "type impl"
</dt> <dt>



Valeur **DWORD** qui contient un jeu d’indicateurs qui définissent les détails d’implémentation du fournisseur. Cette propriété s’applique uniquement aux fournisseurs de stockage de clés. Il peut contenir zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.



| Identificateur                            | Valeur      | Description                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **\_ \_ indicateur matériel de NCRYPT impl \_**      | 0x00000001 | Le fournisseur est basé sur le matériel.                           |
| **\_indicateur du \_ logiciel NCRYPT impl \_**      | 0x00000002 | Le fournisseur est basé sur un logiciel.                           |
| **\_indicateur de \_ déstockage du impl impl \_**     | 0x00000008 | Le fournisseur est amovible.                                |
| **\_indicateur de \_ \_ RNG matériel \_ de NCRYPT impl** | 0x00000010 | Le fournisseur est un générateur de nombres aléatoires basé sur le matériel. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_ \_ propriété type de clé NCRYPT \_**
</dt> <dd> <dl> <dt>

L "type de clé"
</dt> <dt>



Valeur **DWORD** qui contient un jeu d’indicateurs qui définissent le type de clé. Cette propriété s’applique uniquement aux clés. Il peut contenir zéro ou la valeur suivante.



| Identificateur                     | Valeur      | Description                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **\_indicateur de \_ clé d’ordinateur NCRYPT \_** | 0x00000001 | La clé s’applique à l’ordinateur local. Si cet indicateur n’est pas présent, la clé s’applique à l’utilisateur actuel. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**propriété d’utilisation de la \_ clé NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "utilisation de la clé"
</dt> <dt>



Valeur **DWORD** qui contient un jeu d’indicateurs qui définissent les détails d’utilisation d’une clé. Cette propriété s’applique uniquement aux clés. Il peut contenir zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.



| Identificateur                              | Valeur      | Description                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ autoriser le \_ déchiffrement \_**        | 0x00000001 | La clé peut être utilisée pour le déchiffrement.                  |
| **NCRYPT \_ autoriser \_ l' \_ indicateur de signature**        | 0x00000002 | La clé peut être utilisée pour la signature.                     |
| **\_indicateur d' \_ accord de clé d’autorisation NCRYPT \_ \_** | 0x00000004 | La clé peut être utilisée pour le chiffrement de l’accord secret. |
| **NCRYPT \_ autoriser \_ toutes les \_ utilisations**          | 0x00ffffff | La clé peut être utilisée dans n’importe quel but.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**propriété de la \_ dernière \_ modification de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "modifié"
</dt> <dt>



Indique le moment où la clé a été modifiée pour la dernière fois. Ce type de données est un pointeur vers une structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) . Cette propriété s’applique uniquement aux clés persistantes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_propriété de longueur NCRYPT \_**
</dt> <dd> <dl> <dt>

L "longueur"
</dt> <dt>



**Valeur DWORD** qui contient la longueur, en bits, de la clé. Cette propriété s’applique uniquement aux clés.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_propriété de longueurs NCRYPT \_**
</dt> <dd> <dl> <dt>

L « longueurs »
</dt> <dt>



Indique les tailles de clé prises en charge par la clé. Ce type de données est un pointeur vers une structure de [**\_ \_ longueurs pris en charge par NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) qui contient ces informations. Cette propriété s’applique uniquement aux clés.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_propriété de longueur maximale du \_ nom NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "longueur maximale du nom"
</dt> <dt>



**Valeur DWORD** qui contient la longueur maximale, en caractères, du nom d’une clé persistante. Cette propriété s’applique uniquement à un fournisseur.

Cette propriété est principalement destinée à être utilisée par des fournisseurs de stockage de clés qui stockent leurs clés sur un appareil disposant d’une quantité limitée de mémoire disponible, telle qu’une carte à puce.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_propriété de nom NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nom"
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom de l’objet.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**propriété de l' \_ invite du pin NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L « SmartCardPinPrompt »
</dt> <dt>



Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_propriété du pin NCRYPT \_**
</dt> <dd> <dl> <dt>

L « SmartCardPin »
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le code confidentiel. Le code PIN est utilisé pour une clé de carte à puce ou le mot de passe pour une clé protégée par mot de passe stockée dans un KSP basé sur logiciel. Cette propriété ne peut être définie que. Microsoft KSP met en cache cette valeur afin que l’utilisateur ne soit invité qu’une seule fois par processus.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_propriété du \_ handle du fournisseur NCRYPT \_**
</dt> <dd> <dl> <dt>

L "handle du fournisseur"
</dt> <dt>



Un **\_ \_ handle NCRYPT Prov** qui contient le descripteur du fournisseur de stockage de clés CNG. Lorsque vous avez terminé d’utiliser le handle, vous devez appeler [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) pour le libérer.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_propriété de lecteur NCRYPT \_**
</dt> <dd> <dl> <dt>

L « SmartCardReader »
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom du lecteur de carte à puce. Cette propriété ne peut être définie que.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ propriété CERTSTORE racine \_ NCRYPT**
</dt> <dd> <dl> <dt>

L « SmartcardRootCertStore »
</dt> <dt>



**HCERTSTORE** qui représente le magasin de certificats racines de carte à puce.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ ID PIN cicatrice**
</dt> <dd> <dl> <dt>

L « SmartCardPinId »
</dt> <dt>



Pointeur vers la valeur **d' \_ ID de code confidentiel** associée à une [*clé de chiffrement*](/windows/desktop/SecGloss/c-gly) donnée sur une [*carte à puce*](/windows/desktop/SecGloss/s-gly). Il s’agit d’une propriété en lecture seule. Le type de données de l' **\_ ID de code confidentiel** est défini dans cardmod. h.

**Windows Server 2008 et Windows Vista :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_informations de pin cicatrices NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L « SmartCardPinInfo »
</dt> <dt>



Pointeur désignant la structure d' [**\_ informations**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) du code confidentiel associé à une clé de chiffrement donnée sur la carte à puce. L’appelant fournit le handle de clé. Cette propriété est une propriété en lecture seule. La structure d' **\_ informations sur le code confidentiel** est définie dans cardmod. h.

**Windows Server 2008 et Windows Vista :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_propriété de \_ code confidentiel sécurisé NCRYPT \_**
</dt> <dd> <dl> <dt>

L « SmartCardSecurePin »
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le code confidentiel de la session de carte à puce. Cette propriété ne peut être définie que.

**Windows Vista :** Cette propriété n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**propriété de la description de la \_ sécurité NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "descr de sécurité"
</dt> <dt>



Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui contient des informations de contrôle d’accès pour la clé. Cette propriété s’applique uniquement aux clés persistantes. Le paramètre *dwFlags* de la fonction [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) ou [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifie la partie du descripteur de sécurité à récupérer ou à définir.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**\_propriété de \_ \_ prise en charge \_ de la description de la sécurité NCRYPT**
</dt> <dd> <dl> <dt>

L « prise en charge de descr de sécurité »
</dt> <dt>



Indique si le fournisseur prend en charge les descripteurs de sécurité pour les clés. Cette propriété est une **valeur DWORD** qui contient 1 si le fournisseur prend en charge les descripteurs de sécurité pour les clés. Si cette propriété contient une autre valeur, ou si la fonction [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retourne **NPD \_ non \_ pris en charge**, le fournisseur ne prend pas en charge les descripteurs de sécurité pour les clés. Cette propriété s’applique uniquement aux fournisseurs.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_ \_ propriété GUID de la carte à puce NCRYPT \_**
</dt> <dd> <dl> <dt>

L « SmartCardGuid »
</dt> <dt>



Objet BLOB qui contient l’identificateur de la carte à puce.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_propriété de stratégie d’interface utilisateur NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "stratégie d’interface utilisateur"
</dt> <dt>



S’il est utilisé avec la fonction [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) ou [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , il s’agit d’un pointeur vers une structure de [**stratégie d' \_ interface \_ utilisateur NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) qui contient la stratégie d’interface utilisateur de clé forte pour la clé. Cette propriété s’applique uniquement aux clés persistantes. Cette propriété ne peut être définie que lorsque la clé est générée. Une fois que la fonction [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) a été appelée pour cette clé, cette propriété devient en lecture seule.

Un fournisseur de stockage de clés peut recevoir ce paramètre par le biais d’une fonction de rappel [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) . La valeur du paramètre est une \_ \_ structure d’objet blob de stratégie d’interface utilisateur NCRYPT \_ qui contient les mêmes informations. De même, lorsqu’une application envoie une requête via NCryptSetPropertyFn au fournisseur pour retourner cette propriété, le fournisseur est supposé retourner une \_ \_ structure d’objet blob de stratégie d’interface utilisateur NCRYPT \_ .


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_propriété de \_ nom \_ unique NCRYPT**
</dt> <dd> <dl> <dt>

L "nom unique"
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom unique de l’objet. Il s’agit d’un autre nom qui peut être utilisé lors de l’accès à la clé. Cette propriété est utilisée lorsqu’il est supposé que le nom de clé initialement passé à [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) n’est pas suffisamment unique pour identifier de manière fiable la clé persistante. Le fournisseur de stockage de clés Microsoft renverra le nom de fichier de la clé en tant que propriété.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**\_propriété de \_ contexte d’utilisation NCRYPT \_**
</dt> <dd> <dl> <dt>

L "utiliser le contexte"
</dt> <dt>



Pointeur vers une chaîne Unicode terminée par le caractère null qui décrit le contexte de l’opération. Cette propriété n’est pas persistante et peut être définie soit sur un fournisseur, soit sur une clé. Une clé n’a pas accès à la propriété de **\_ propriété de \_ contexte \_ NCRYPT use** du fournisseur, car la propriété est spécifique uniquement au handle pour lequel elle est définie.

Un fournisseur de stockage de clés qui doit inviter l’utilisateur lors d’un appel à [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (par exemple, «insérez votre carte à puce dans le lecteur) est un exemple dans lequel cette propriété serait utilisée dans le contexte d’un fournisseur. Étant donné que le handle de clé n’est pas disponible tant que **NCryptOpenKey** n’a pas retourné la valeur, l’application doit définir cette propriété sur le handle du fournisseur avant d’appeler **NCryptOpenKey**.

Voici un exemple dans lequel cette propriété serait utilisée dans le contexte d’un handle de clé. il s’agit d’un fournisseur de stockage de clés qui doit inviter l’utilisateur pendant une opération à l’aide de la clé (par exemple, « cette application a besoin d’utiliser cette clé pour signer un document. »). Le fournisseur peut ensuite relayer ces informations de contexte à l’utilisateur dans n’importe quelle interface utilisateur affichée pendant l’opération.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_propriété NCRYPT use \_ Count \_ enabled \_**
</dt> <dd> <dl> <dt>

L "nombre d’utilisations activées
</dt> <dt>



Indique si le fournisseur prend en charge le comptage de l’utilisation des clés. Cette propriété est une **valeur DWORD** qui contient 1 si le fournisseur prend en charge le comptage de l’utilisation des clés. Si cette propriété contient une autre valeur, ou si la fonction [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retourne **NPD \_ non \_ pris en charge**, le fournisseur ne prend pas en charge le comptage de l’utilisation des clés. Cette propriété s’applique uniquement aux fournisseurs.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_propriété du \_ nombre d’utilisations de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nombre d’utilisations"
</dt> <dt>



Variable [**de \_ type entier ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) qui contient le nombre d’opérations effectuées par la [*clé privée*](/windows/desktop/SecGloss/p-gly) spécifiée. Cette propriété est facultative et peut ne pas être prise en charge par tous les fournisseurs. Les fournisseurs qui prennent en charge cette propriété sur les clés doivent également prendre en charge la propriété de **\_ propriété NCRYPT use \_ Count \_ enabled \_** sur le descripteur du fournisseur. Le fournisseur de stockage de clés Microsoft ne prend pas en charge cette propriété. Cette propriété s’applique uniquement aux clés persistantes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ propriété CERTSTORE de l’utilisateur NCRYPT \_**
</dt> <dd> <dl> <dt>

L « SmartCardUserCertStore »
</dt> <dt>



**HCERTSTORE** qui représente le magasin de certificats utilisateur de carte à puce.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_propriété de version NCRYPT \_**
</dt> <dd> <dl> <dt>

L "version"
</dt> <dt>



**Valeur DWORD** qui contient la version du logiciel du fournisseur. Le mot de poids fort contient la version principale et le mot de poids faible contient la version mineure. Par exemple, 0x00030033 = 3,51. Cette propriété s’applique uniquement aux fournisseurs.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_propriété du \_ handle de fenêtre NCRYPT \_**
</dt> <dd> <dl> <dt>

L "handle HWND"
</dt> <dt>



Pointeur vers le handle de fenêtre (**HWND**) à utiliser comme parent de toute interface utilisateur affichée.

Comme un comportement indésirable peut se produire lorsqu’une interface utilisateur est affichée à l’aide d’un handle de fenêtre **null** pour le parent, nous vous recommandons vivement qu’un fournisseur de stockage de clés n’affiche pas d’interface utilisateur, sauf si cette propriété est définie.


</dt> </dl> </dd> </dl>

Les valeurs suivantes sont utilisées pour définir les limites des données de propriété.



| Constante/valeur                                                                                                                                                                                                                                                 | Description                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ Nombre maximal de \_ \_ données de propriété**</dt> <dt></dt> </dl> | Spécifie la taille maximale, en octets, d’une valeur de propriété.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ \_ \_ Nom de propriété max**</dt> <dt>64</dt> </dl>       | Spécifie la taille maximale d’un nom de propriété, en caractères.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Ncrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

