---
description: Crée un certificat X. 509, signé par la clé racine de test ou une autre clé spécifiée, qui lie votre nom à la partie publique de la paire de clés. Le certificat est enregistré dans un fichier, un magasin de certificats système, ou les deux.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff9fb79b5db5a6a71eee981166742b4e1680184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471925"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> MakeCert est déconseillé. Pour créer des certificats auto-signés, utilisez l’applet de commande PowerShell [New-SelfSignedCertificate](/powershell/module/pki/new-selfsignedcertificate).

 

L’outil MakeCert crée un certificat [*X. 509*](../secgloss/x-gly.md) , signé par la clé racine de test ou une autre clé spécifiée, qui lie votre nom à la partie publique de la paire de clés. Le certificat est enregistré dans un fichier, un magasin de certificats système, ou les deux. l’outil est installé dans le \\ dossier Bin du chemin d’installation du kit de développement logiciel (SDK) de Microsoft Windows.

L’outil MakeCert utilise la syntaxe de commande suivante :

**Makecert** \[ *BasicOptions* \| *ExtendedOptions* \] *FichierSortie*

*FichierSortie* est le nom du fichier dans lequel le certificat sera écrit. Vous pouvez omettre *outputfile* si le certificat ne doit pas être écrit dans un fichier.

## <a name="options"></a>Options

MakeCert comprend des options de base et étendues. Les options de base sont celles le plus fréquemment utilisées lors de la création d'un certificat. Les options avancées offrent une flexibilité accrue.

Les options de MakeCert sont également divisées en trois groupes fonctionnels :

-   Options de base spécifiques à la technologie du magasin de certificats uniquement.
-   Options étendues spécifiques à la technologie de fichier SPC et de clé privée uniquement.
-   Options étendues applicables à la technologie du fichier SPC, de la clé privée et du magasin de certificats.

Les options indiquées dans les tableaux suivants peuvent être utilisées uniquement avec Internet Explorer 4,0 ou version ultérieure.




| Option de base | Description | 
|--------------|-------------|
| <strong>-a</strong> <strong></strong> <em>Algorithme</em> | Algorithme de <a href="/windows/desktop/SecGloss/h-gly"><em>hachage</em></a> . Doit avoir la valeur <strong>SHA-1</strong> ou <strong>MD5</strong> (valeur par défaut). Pour plus d’informations sur MD5, consultez <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>. | 
| <strong>-b</strong> <strong></strong> <em>DateStart</em> | Date à laquelle le certificat devient valide. La valeur par défaut est lorsque le certificat est créé. Le format de <em>DateStart</em> est mm/jj/aaaa. | 
| <strong>-CY</strong> <strong></strong> <em>CertificateTypes</em> | Type de certificat. <em>CertificateTypes</em> peut être <strong>end</strong> pour l’entité finale ou l' <strong>autorité</strong> de <a href="/windows/desktop/SecGloss/c-gly"><em>certification</em></a>. | 
| <strong>-e</strong> <strong></strong> <em>DateEnd</em> | Date de fin de la période de validité. La valeur par défaut est l’année 2039. | 
| <strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong><em>OID2</em> ... | Insère dans le certificat une liste d’un ou de plusieurs<a href="/windows/desktop/SecGloss/o-gly"><em>identificateurs d’objet</em></a> (OID) séparés <a href="/windows/desktop/SecGloss/e-gly"><em>par des virgules, séparés</em></a>par des virgules. Par exemple, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> insère l’OID d’authentification du client. Pour obtenir les définitions des OID autorisés, consultez le fichier Wincrypt. h dans CryptoAPI 2.0. | 
| <strong>-h</strong> <strong></strong> <em>NumChildren</em> | Hauteur maximale de l’arborescence en dessous de ce certificat. | 
| <strong>-l</strong> <strong></strong> <em>PolicyLink</em> | Lien vers les informations de stratégie de l’Agence SPC (par exemple, une URL). | 
| <strong>-m</strong> <strong></strong> <em>nMonths</em> | Durée de la période de validité. | 
| <strong>-n</strong><strong>"</strong><em>nom</em><strong>"</strong> | Nom du certificat de l’éditeur. Ce nom doit être conforme à la norme <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> . La méthode la plus simple consiste à utiliser le format « CN =<em>myname</em>». Par exemple : <strong>-n "CN = test"</strong>. | 
| <strong>-nscp</strong> | L’extension d’authentification du client Netscape doit être incluse. | 
| <strong>-PE</strong> | Marque la clé privée comme étant exportable. | 
| <strong>-r</strong> | Crée un certificat auto-signé | 
| <strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em> | Nom du fichier de certificat avec la clé publique du sujet existant à utiliser. | 
| <strong>-SK</strong> <strong></strong> <em>SubjectKey</em> | Emplacement du conteneur de clé du sujet qui contient la <a href="/windows/desktop/SecGloss/p-gly"><em>clé privée</em></a>. Un conteneur de clé sera créé s'il n'en existe aucun. Si aucune des options <strong>-SK</strong> ou <strong>-SV</strong> n’est utilisée, un conteneur de clé par défaut est créé et utilisé par défaut. | 
| <strong>-ciel</strong> <strong></strong> <em>SubjectKeySpec</em> | Spécification de clé du sujet. <em>SubjectKeySpec</em> doit avoir l’une des trois valeurs possibles :<br /><ul><li><strong>Signature</strong> (spécification de clé AT_SIGNATURE)</li><li><strong>Exchange</strong> (spécification de clé AT_KEYEXCHANGE)</li><li>Entier, tel que <strong>3</strong></li></ul>Pour plus d’informations, consultez la remarque qui suit ce tableau.<br /> | 
| <strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em> | Fournisseur CryptoAPI pour l’objet. La valeur par défaut est le fournisseur de l’utilisateur. Pour plus d’informations sur les fournisseurs CryptoAPI, consultez la documentation CryptoAPI 2.0. | 
| <strong>-SR</strong> <strong></strong> <em>SubjectCertStoreLocation</em> | Emplacement du Registre du magasin de certificats du sujet. <em>SubjectCertStoreLocation</em> doit être <strong>LocalMachine</strong> (clé de Registre HKEY_LOCAL_MACHINE) ou <strong>CurrentUser</strong> (clé de Registre HKEY_CURRENT_USER). <strong>CurrentUser</strong> est la valeur par défaut. | 
| <strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em> | Nom du magasin de certificats du sujet dans lequel le certificat généré sera stocké. | 
| <strong>-SV</strong> <strong></strong> <em>SubjectKeyFile</em> | Nom du fichier. pvk du sujet. Si aucune des options <strong>-SK</strong> ou <strong>-SV</strong> n’est utilisée, un conteneur de clé par défaut est créé et utilisé par défaut. | 
| <strong>-SY</strong> <strong></strong> <em>nSubjectProviderType</em> | Type de fournisseur CryptoAPI pour l’objet. La valeur par défaut est <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Pour plus d’informations sur les types de fournisseur CryptoAPI, consultez la documentation CryptoAPI 2.0. | 
| <strong>-#</strong><strong></strong><em>SerialNumber</em> | Numéro de série du certificat. La valeur maximale est 2 ^ 31. La valeur par défaut est une valeur générée par l’outil qui est garantie comme étant unique. | 
| <strong>-$</strong><strong></strong><em>CertificateAuthority</em> | Type d' <a href="/windows/desktop/SecGloss/c-gly"><em>autorité de certification</em></a>. <em>CertificateAuthority</em> doit être défini sur <strong>commercial</strong> (pour les certificats utilisés par les éditeurs de logiciels commerciaux) ou sur <strong>individuel</strong> (pour les certificats utilisés par les éditeurs de logiciels individuels). | 
| <strong>-?</strong> | Affiche les options de base. | 
| <strong>-!</strong> | Affiche les options étendues. | 




 

> [!Note]  
> Si l’option **de spécification de clé-ciel** est utilisée dans Internet Explorer version 4,0 ou ultérieure, la spécification doit correspondre à la spécification de clé indiquée par le fichier de [*clé privée*](../secgloss/p-gly.md) ou le [*conteneur de clé*](../secgloss/k-gly.md)privée. Si l’option de spécification de clé n’est pas utilisée, la spécification de clé indiquée par le fichier de clé privée ou le conteneur de clé privée sera utilisée. S’il existe plus d’une spécification de clé dans le conteneur de clé, MakeCert tente d’abord d’utiliser la \_ spécification de clé at signature. En cas d’échec, MakeCert essaiera d’utiliser AT \_ KeyExchange. Étant donné que la plupart des utilisateurs ont une clé AT de \_ signature ou une \_ clé at KeyExchange, cette option n’a pas besoin d’être utilisée dans la plupart des cas.

 

les options suivantes sont uniquement destinées aux fichiers SPC ( [*Software Publisher certificate*](../secgloss/s-gly.md) ) et à la technologie de clé privée.




| Option SPC et clé privée | Description | 
|----------------------------|-------------|
| <strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em> | Emplacement du certificat de l’émetteur. | 
| <strong>-ik</strong> <strong></strong> <em>IssuerKey</em> | Emplacement du conteneur de clé de l’émetteur. La valeur par défaut est la clé racine de test. | 
| <strong>-IKY</strong> <strong></strong> <em>IssuerKeySpec</em> | Spécification de clé de l’émetteur, qui doit être l’une des trois valeurs possibles :<br /><ul><li><strong>Signature</strong> (spécification de clé AT_SIGNATURE)</li><li><strong>Exchange</strong> (spécification de clé AT_KEYEXCHANGE)</li><li>Entier, tel que <strong>3</strong></li></ul>Pour plus d’informations, consultez la remarque qui suit ce tableau.<br /> | 
| <strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em> | Fournisseur CryptoAPI pour l’émetteur. La valeur par défaut est le fournisseur de l’utilisateur. Pour plus d’informations sur les fournisseurs CryptoAPI, consultez la documentation CryptoAPI 2.0. | 
| <strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em> | Fichier de clé privée de l’émetteur. La valeur par défaut est la racine de test. | 
| <strong>-e/e</strong> <strong></strong> <em>nIssuerProviderType</em> | Type de fournisseur CryptoAPI pour l’émetteur. La valeur par défaut est <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Pour plus d’informations sur les types de fournisseur CryptoAPI, consultez la documentation CryptoAPI 2.0. | 




 

> [!Note]  
> Si l’option de spécification de clé **-IKY** est utilisée dans Internet Explorer 4,0 ou une version ultérieure, la spécification doit correspondre à la spécification de clé indiquée par le fichier de [*clé privée*](../secgloss/p-gly.md) ou le [*conteneur de clé*](../secgloss/k-gly.md)privée. Si l’option de spécification de clé n’est pas utilisée, la spécification de clé indiquée par le fichier de clé privée ou le conteneur de clé privée sera utilisée. S’il existe plus d’une spécification de clé dans le conteneur de clé, MakeCert tente d’abord d’utiliser la \_ spécification de clé at signature. En cas d’échec, MakeCert essaiera d’utiliser AT \_ KeyExchange. Étant donné que la plupart des utilisateurs ont une clé AT de \_ signature ou une \_ clé at KeyExchange, cette option n’a pas besoin d’être utilisée dans la plupart des cas.

 

Les options suivantes sont destinées uniquement à la technologie du [*magasin de certificats*](../secgloss/c-gly.md) .



| Option du magasin de certificats          | Description                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-IC** *IssuerCertFile*          | Fichier qui contient le certificat de l’émetteur. MakeCert recherche un certificat avec une correspondance exacte dans le magasin de certificats.                                                                                                                                                                                                        |
| **-dans** *IssuerNameString*        | Nom commun du certificat de l’émetteur. MakeCert recherche un certificat dont le nom commun comprend *IssuerNameString* dans le magasin de certificats.                                                                                                                                                                                  |
| **-IR** *IssuerCertStoreLocation* | Emplacement du Registre du magasin de certificats de l’émetteur. *IssuerCertStoreLocation* doit être **LocalMachine** (clé de Registre HKEY \_ local \_ machine) ou **CurrentUser** (clé de Registre HKEY \_ Current \_ User). **CurrentUser** est la valeur par défaut.                                                                                                |
| **-est** *IssuerCertStoreName*     | Magasin de certificats de l’émetteur qui comprend le certificat de l’émetteur et ses informations de clé privée associées. S’il existe plus d’un certificat dans le magasin, l’utilisateur doit l’identifier de manière unique à l’aide de l’option **-IC** ou **-in** . Si le certificat dans le magasin de certificats n’est pas identifié de manière unique, MakeCert échoue. |



 

 

 
