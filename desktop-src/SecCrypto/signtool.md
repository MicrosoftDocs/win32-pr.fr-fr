---
title: SignTool (SignTool)
description: SignTool est un outil en ligne de commande qui signe numériquement les fichiers, vérifie les signatures dans les fichiers et les fichiers d’horodatage.
ms.assetid: aa59cb35-5fba-4ce8-97ea-fc767c83f88e
ms.topic: article
ms.date: 10/12/2020
ms.openlocfilehash: 884d4c132a2877a51cef7610dd32e8ef6b9c4bc3
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "104383187"
---
# <a name="signtool"></a>SignTool (SignTool)

SignTool est un outil en ligne de commande qui signe numériquement les fichiers, vérifie les signatures dans les fichiers et les fichiers d’horodatage. Pour plus d’informations sur la raison pour laquelle la signature des fichiers est importante, consultez [Présentation de la signature de code](cryptography-tools.md). L’outil est installé dans le \\ dossier bin du chemin d’installation du kit de développement logiciel (SDK) Microsoft Windows.

SignTool est disponible dans le cadre de la SDK Windows, que vous pouvez télécharger à partir de <https://developer.microsoft.com/windows/downloads/windows-10-sdk/> .

> [!Note]  
> Les **versions 20236 et ultérieures** du kit de développement logiciel (SDK) Windows 10, Windows 10 HLK, Windows 10 WDK et Windows 10 ADK requièrent désormais la spécification de l’algorithme Digest. La commande de signature SignTool requiert la `file digest algorithm` spécification de/FD et de l' `timestamp digest algorithm` option/TD lors de la signature et de l’horodatage, respectivement. Un avertissement (code d’erreur 0, initialement) est levé si/FD n’est pas spécifié lors de la signature et si/TD n’est pas spécifié lors de l’horodatage. Dans les versions ultérieures de SignTool, l’avertissement devient une erreur. SHA256 est recommandé et est considéré comme plus sûr que SHA1 par le secteur.  


## <a name="syntax"></a>Syntaxe  
  
```console  
signtool [command] [options] [file_name | ...]  
```  

## <a name="parameters"></a>Paramètres  
  
|Argument|Description|  
|----|----|  
|`command`|L'une des quatre commandes (`catdb`, `sign`, `Timestamp` ou `Verify`) qui spécifie une opération à exécuter sur un fichier. Pour obtenir une description de chaque commande, consultez le tableau suivant.|  
|`options`|Une option qui modifie une commande. En plus des options globales `/q` et `/v`, chaque commande prend en charge un seul ensemble d'options.|  
|`file_name`|Le chemin d’accès à un fichier à signer.| 


Les commandes suivantes sont prises en charge par SignTool.

|Commande|Description|  
|----|----|  
|`Catdb`|Ajoute ou supprime un fichier catalogue dans une base de données de catalogue. Les bases de données de catalogue sont utilisées pour la récupération automatique des fichiers catalogue et sont identifiées par un GUID. Pour obtenir la liste des options prises en charge par la commande `catdb`, consultez [Options de commande catdb](/dotnet/framework/tools/signtool-exe#catdb-command-options).|  
|`Sign`|Signe numériquement les fichiers. Les signatures numériques protègent les fichiers contre la falsification et permettent aux utilisateurs de vérifier le signataire selon un certificat de signature. Pour obtenir la liste des options prises en charge par la commande `sign`, consultez [Options de commande sign](/dotnet/framework/tools/signtool-exe#sign-command-options).|  
|`Timestamp`|Horodate les fichiers. Pour obtenir la liste des options prises en charge par la commande `TimeStamp`, consultez [Options de commande TimeStamp](/dotnet/framework/tools/signtool-exe#timestamp-command-options).|  
|`Verify`|Vérifie la signature numérique des fichiers en déterminant si le certificat de signature a été publié par une autorité de confiance, si le certificat de signature a été révoqué et, éventuellement, si le certificat de signature est valide pour une stratégie spécifique. Pour obtenir la liste des options prises en charge par la commande `Verify`, consultez [Options de commande Verify](/dotnet/framework/tools/signtool-exe#verify-command-options).|

 Les options suivantes s'appliquent à toutes les commandes de l'outil Signature.  
  
|Option globale|Description|  
|----|----|  
|**/q**|N'affiche aucune sortie si la commande fonctionne correctement, et affiche la sortie minimale si la commande échoue.|  
|**/v**|Affiche la sortie des commentaires que la commande s'exécute correctement ou échoue, et affiche des messages d'avertissement.|  
|**/Debug**|Affiche les informations de débogage.|  

 
## <a name="catdb-command-options"></a>Options de commande CatDB  

 Le tableau suivant répertorie les options qui peuvent être utilisées avec la commande `Catdb`.

| Option Catdb | Description |
|----|----| 
| **/d** | Spécifie que la base de données de catalogue par défaut doit être mise à jour. Si les options **/d** et **/g** ne sont pas utilisées, SignTool met à jour la base de données des pilotes et des composants système. |
| **/G** *GUID* | Spécifie que la base de données de catalogue identifiée par le GUID doit être mise à jour.|
| **/r** | Supprime le catalogue spécifié de la base de données du catalogue. Si cette option n’est pas spécifiée, SignTool ajoute le catalogue spécifié à la base de données du catalogue.|
| **/u.** | Spécifie qu’un nom unique doit être généré automatiquement pour les fichiers catalogue ajoutés. Si nécessaire, les fichiers catalogue seront renommés pour empêcher des conflits entre les noms des fichiers catalogue existants. Si cette option n’est pas spécifiée, SignTool remplace tout catalogue existant qui porte le même nom que le catalogue ajouté.|

> [!Note]  
> Les bases de données de catalogue sont utilisées pour la recherche automatique de fichiers de catalogue.


## <a name="sign-command-options"></a>Options de la commande Sign  

 Le tableau suivant répertorie les options qui peuvent être utilisées avec la commande `sign`.  
  
|Options de la commande Sign|Description|  
|----|----| 
|`/a`|Sélectionne automatiquement le meilleur certificat de signature. L'outil Signature recherche tous les certificats valides qui répondent à toutes les conditions spécifiées et sélectionne celui qui est valide le plus longtemps. Si cette option n'est pas présente, l'outil Signature pense trouver un seul certificat de signature valide.|  
|`/ac`  *fichier*|Ajoute un certificat supplémentaire à partir de *file* au bloc de signature.|  
|`/as`|Ajoute cette signature. Si aucune signature principale n'est présente, cette signature est effectuée à la signature principale à la place.|  
|`/c`  *CertTemplateName*|Spécifie le nom du modèle de certificat (une extension Microsoft) pour le certificat de signature.|  
|`/csp`  *CSPName*|Spécifie le fournisseur de services de chiffrement (CSP) qui contient le conteneur de clés privées.|  
|`/d`  *DESC*|Spécifie une description du contenu signé.|  
|`/dg`  *D*|Génère le condensé à signer et les fichiers PKCS7 non signés. Les fichiers de sortie Digest et PKCS7 sont les suivants : *Path\FileName.Dig* et *Path\FileName.p7u*. Pour générer un fichier XML supplémentaire, consultez <strong>/DXML</strong>.|  
|`/di`  *D*|Crée la signature en ingestion du condensé signé dans le fichier PKCS7 non signé. Les fichiers de résumé et PKCS7 non signés d’entrée doivent être : *Path\FileName.Dig.signed* et *Path\FileName.p7u*.|  
|`/dlib`  *DLL*|Spécifie la DLL qui implémente la <code>AuthenticodeDigestSign</code> fonction avec laquelle signer le Digest. Cette option équivaut à utiliser <strong>SignTool</strong> séparément avec les commutateurs <strong>/DG</strong>, <strong>/DS</strong>et <strong>/di</strong> , sauf que cette option appelle les trois une seule opération atomique.|  
|`/dmdf`  *Extension*|Lorsqu’il est utilisé avec l’option <strong>/DG</strong> , passe le contenu du fichier à la <code>AuthenticodeDigestSign</code> fonction sans modification.|  
|`/ds`  |Signe le condensé uniquement. Le fichier d’entrée doit être le Digest généré par l’option <strong>/DG</strong> . Le fichier de sortie sera : *file. signed*.|  
|`/du`  *URL*|Spécifie une URL pour la description développée du contenu signé.|  
|`/dxml`  |Lorsqu’il est utilisé avec l’option <strong>/DG</strong> , produit un fichier XML. Le fichier de sortie est le suivant : *Path\FileName.dig.xml*.|  
|`/f`  *SignCertFile*|Spécifie le certificat de signature dans un fichier. Si le fichier est au format PFX (Personal Information Exchange) et protégé par un mot de passe, utilisez l'option `/p` pour spécifier le mot de passe. Si le fichier ne contient aucune clé privée, utilisez les options `/csp` et `/kc` pour spécifier le nom du conteneur CSP et de clés privées.|  
|`/fd`*ALG*|Spécifie l’algorithme de condensat de fichiers à utiliser pour créer des signatures de fichiers. </br> **Remarque :** Un avertissement est généré si l’option <strong>/FD</strong> n’est pas spécifiée lors de la signature. L’ALG par défaut est SHA1 mais SHA256 est recommandé.|
|`/fd`  *certHash*|La spécification de la chaîne certHash aura comme valeur par défaut l’algorithme utilisé sur le certificat de signature. </br> **Remarque :** Disponible uniquement dans les versions 20236 et ultérieures du Kit Windows 10.|  
|`/i`  *IssuerName*|Spécifie le nom de l'émetteur du certificat de signature. Cette valeur peut être une sous-chaîne du nom d'émetteur entier.|  
|`/kc`  *PrivKeyContainerName*|Spécifie le nom du conteneur de clés privées.|  
|`/n`  *SubjectName*|Spécifie le nom de l'objet du certificat de signature. Cette valeur peut être une sous-chaîne du nom de l'objet entier.|  
|`/nph`|En cas de prise en charge, supprime les hachages de pages pour les fichiers exécutables. La valeur par défaut est déterminée par la variable d'environnement SIGNTOOL_PAGE_HASHES et par la version de wintrust.dll. Cette option est ignorée pour les fichiers non PE.|  
|`/p`  *Mot de passe*|Spécifie le mot de passe à utiliser lors de l'ouverture d'un fichier PFX. (Utilisez l'option `/f` pour spécifier un fichier PFX.)|  
|`/p7` *Chemin*|Spécifie qu'un fichier PKCS (Public Key Cryptography Standards) #7 est produit pour chaque fichier de contenu spécifié. Les fichiers de #7 PKCS sont nommés *chemin* \\ *nom_de_fichier*. P7.|  
|`/p7ce` *Valeur*|Spécifie des options pour le contenu PKCS #7 signé. Remplacez *Value* par « Embedded » pour incorporer le contenu signé dans le fichier PKCS #7 ou par « DetachedSignedData » pour produire la partie signée des données d’un fichier PKCS #7 détaché. Si l'option `/p7ce` n'est pas utilisée, le contenu signé est incorporé par défaut.|  
|`/p7co` *\<OID>*|Spécifie l'identificateur d'objet (OID) qui identifie le contenu PKCS #7 signé.|  
|`/ph`|En cas de prise en charge, génère les hachages de pages pour les fichiers exécutables.|  
|`/r`  *RootSubjectName*|Spécifie le nom de l'objet du certificat racine auquel le certificat de signature doit être lié. Cette valeur peut être une sous-chaîne du nom de l'objet entier du certificat racine.|  
|`/s`  *StoreName*|Spécifie le magasin à ouvrir lors de la recherche du certificat. Si cette option n'est pas spécifiée, le magasin `My` est ouvert.|  
|`/sha1`  *Format*|Spécifie le hachage SHA1 du certificat de signature. Le hachage SHA1 est souvent spécifié lorsque plusieurs certificats répondent aux critères spécifiés par les commutateurs restants.|  
|`/sm`|Spécifie qu'un magasin d'ordinateur, au lieu d'un magasin d'utilisateur, est utilisé.|  
|`/t`  *URL*|Spécifie l'URL du serveur d'horodatage. Si cette option (ou `/tr`) n'est pas présente, le fichier signé ne sera pas horodaté. Un avertissement est généré si l'horodatage échoue. Cette option ne peut pas être utilisée avec l'option `/tr`.|  
|`/td`  *ALG*|Utilisé avec l'option `/tr` pour demander un algorithme Digest utilisé par le serveur d'horodatage RFC 3161. </br> **Remarque :** Un avertissement est généré si le commutateur <strong>/TD</strong> n’est pas fourni lors de l’horodatage. L’ALG par défaut est SHA1 mais SHA256 est recommandé. <br/> Le commutateur <strong>/TD</strong> doit être déclaré après le commutateur <strong>/TR</strong> , et non avant. Si le commutateur <strong>/TD</strong> est déclaré avant le commutateur <strong>/TR</strong> , l’horodateur retourné est issu d’un algorithme SHA1 au lieu de l’algorithme SHA256 prévu. |
|`/tr`  *URL*|Spécifie l'URL du serveur d'horodatage RFC 3161. Si cette option (ou `/t`) n'est pas présente, le fichier signé ne sera pas horodaté. Un avertissement est généré si l'horodatage échoue. Cette option ne peut pas être utilisée avec l'option `/t`.|  
|`/u`  *Utilisation*|Spécifie l'utilisation améliorée de la clé (EKU) qui doit être présente dans le certificat de signature. La valeur de l'utilisation peut être spécifiée par un OID ou une chaîne. L'utilisation par défaut est « Signature du code » (1.3.6.1.5.5.7.3.3).|  
|`/uw`|Spécifie l'utilisation « Windows System Component Verification » (1.3.6.1.4.1.311.10.3.6).|  
  
 Pour obtenir des exemples, consultez [Utilisation de SignTool pour signer un fichier](using-signtool-to-sign-a-file.md).  
  

## <a name="timestamp-command-options"></a>Options de commande TimeStamp  

 Le tableau suivant répertorie les options qui peuvent être utilisées avec la commande `TimeStamp`.  
  
|Option TimeStamp|Description|  
|----|----|  
|`/p7`|Horodate les fichiers PKCS #7.|  
|`/t`  *URL*|Spécifie l'URL du serveur d'horodatage. Le fichier en cours d'horodatage doit avoir été signé au préalable. L'option `/t` ou `/tr` est obligatoire.|  
|`/td`  *ALG*|Utilisé avec l'option `/tr` pour demander un algorithme Digest utilisé par le serveur d'horodatage RFC 3161. </br> **Remarque :** Un avertissement est généré si le commutateur <strong>/TD</strong> n’est pas fourni lors de l’horodatage. L’ALG par défaut est SHA1 mais SHA256 est recommandé. <br/> Le commutateur <strong>/TD</strong> doit être déclaré après le commutateur <strong>/TR</strong> , et non avant. Si le commutateur <strong>/TD</strong> est déclaré avant le commutateur <strong>/TR</strong> , l’horodateur retourné est issu d’un algorithme SHA1 au lieu de l’algorithme SHA256 prévu. |
|`/tp`*index*|Horodate la signature à l’*index*.|  
|`/tr`  *URL*|Spécifie l'URL du serveur d'horodatage RFC 3161. Le fichier en cours d'horodatage doit avoir été signé au préalable. L'option `/tr` ou `/t` est obligatoire.|  


## <a name="verify-command-options"></a>Options de commande Verify  

|Option Verify|Description|
|----|----|
| **/a** | Spécifie que toutes les méthodes peuvent être utilisées pour vérifier le fichier. En premier lieu, une recherche est effectuée dans les bases de données de catalogue pour déterminer si le fichier est signé dans un catalogue. Si le fichier n’est signé dans aucun catalogue, SignTool tente de vérifier la signature incorporée du fichier. Cette option est recommandée lors de la vérification de fichiers qui peuvent être ou non signés dans un catalogue. Les fichiers ou pilotes Windows sont des exemples de fichiers qui peuvent être ou non signés. |
| **/ad** | Recherche le catalogue à l'aide de la base de données de catalogue par défaut. |
| **All** | Vérifie toutes les signatures dans un fichier avec plusieurs signatures. |
| **/as** | Recherche le catalogue à l'aide de la base de données de catalogue du composant système (pilote). |
| **/AG** *CatDBGUID* | Recherche le catalogue dans la base de données du catalogue identifié par le **GUID**. |
| **/c** *CatFile* | Spécifie le fichier catalogue par nom. |
| **/d** | Imprimez la description et l’URL de description.<br/> **Windows Vista et versions antérieures :** Cet indicateur n’est pas pris en charge.<br/> |
| l' *index* **/DS** | Vérifie la signature à une certaine position. |
| **/hash**{**SHA1** \| **SHA256**} | Spécifie un algorithme de hachage facultatif à utiliser lors de la recherche d'un fichier dans un catalogue. |
| **/kp** | Effectue la vérification à l’aide de la stratégie de signature de pilotes en mode noyau x64. |
| **/ms.** | Utilise plusieurs sémantiques de vérification. Il s’agit du comportement par défaut d’un appel [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) . |
|  *version* /o | Vérifie le fichier par version du système d'exploitation. Le paramètre version se présente sous la forme suivante :<br/> *PlatformID ***:*** VerMajor ***.*** Vermine ***.*** BuildNumber*<br/> L’utilisation du commutateur */o* est recommandée. Si */o* n’est pas spécifié, SignTool peut retourner des résultats inattendus. Par exemple, si vous n’incluez pas le commutateur */o* , les catalogues système qui valident correctement sur un système d’exploitation plus ancien peuvent ne pas valider correctement sur un système d’exploitation plus récent. |
| **/p7** | Vérifiez les \# fichiers PKCS 7. Aucune stratégie existante n’est utilisée pour la \# validation PKCS 7. La signature est vérifiée et une chaîne est générée pour le certificat de signature. |
| **/pa** | Spécifie que la stratégie de vérification de l’authentification par défaut est utilisée. Si l’option **/PA** n’est pas spécifiée, SignTool utilise la stratégie de vérification des pilotes Windows. Cette option ne peut pas être utilisée avec les options **CatDB** . |
| **/PG** *PolicyGUID* | Spécifie une stratégie de vérification par **GUID**. Le **GUID** correspond à l’ActionID de la stratégie de vérification. Cette option ne peut pas être utilisée avec les options **CatDB** . |
| **/pH** | Imprimer et vérifier les valeurs de hachage de la page.<br/> **Windows Vista et versions antérieures :** Cet indicateur n’est pas pris en charge.<br/>  |
| **/R** *RootSubjectName* | Spécifie le nom de l'objet du certificat racine auquel le certificat de signature doit être lié. Cette valeur peut être une sous-chaîne du nom de l'objet entier du certificat racine. |
| **/tw** | Spécifie qu’un avertissement est généré si la signature n’est pas horodatée.|


La commande SignTool **verify** détermine si le certificat de signature a été émis par une autorité de confiance, si le certificat de signature a été révoqué et, éventuellement, si le certificat de signature est valide pour une stratégie spécifique.  

La commande SignTool **verify** génère l’état de la signature **incorporée** , sauf si une option est spécifiée pour rechercher un catalogue (/a,/ad,/As,/AG,/c).


## <a name="return-value"></a>Valeur retournée  

 L'outil Signature retourne l'un des codes de sortie suivants lorsqu'il se termine.  
  
|Code de sortie|Description|  
|----|----| 
|0|L'exécution a été correctement effectuée.|  
|1|L'exécution a échoué.|  
|2|L'exécution a été effectuée avec des avertissements.|


## <a name="examples"></a>Exemples  

 La commande suivante ajoute le fichier catalogue MyCatalogFileName.cat au composant système et à la base de données de pilotes. L'option `/u` génère un nom unique si nécessaire pour éviter de remplacer un fichier catalogue existant nommé `MyCatalogFileName.cat`.  
  
```console  
signtool catdb /v /u MyCatalogFileName.cat  
```  
  
 La commande suivante signe un fichier automatiquement à l'aide du meilleur certificat.  
  
```console  
signtool sign /a /fd SHA256 MyFile.exe 
```  
  
 La commande suivante signe numériquement un fichier à l'aide d'un certificat stocké dans un fichier PFX protégé par un mot de passe.  
  
```console  
signtool sign /f MyCert.pfx /p MyPassword /fd SHA256 MyFile.exe 
```  
  
 La commande suivante signe numériquement et horodate un fichier. Le certificat utilisé pour signer le fichier est stocké dans un fichier PFX.  
  
```console  
signtool sign /f MyCert.pfx /t http://timestamp.digicert.com /fd SHA256 MyFile.exe 
```  
  
 La commande suivante signe un fichier à l'aide d'un certificat situé dans le magasin `My` qui a un nom d'objet `My Company Certificate`.  
  
```console  
signtool sign /n "My Company Certificate" /fd SHA256 MyFile.exe 
```  
  
 La commande suivante signe un contrôle ActiveX et fournit des informations qui sont affichées par Internet Explorer lorsque l'utilisateur est invité à installer le contrôle.  
  
```console  
Signtool sign /f MyCert.pfx /d: "MyControl" /du http://www.example.com/MyControl/info.html /fd SHA256 MyControl.exe 
```  
  
 La commande suivante horodate à un fichier qui a déjà été signé numériquement.  
  
```console  
signtool timestamp /t http://timestamp.digicert.com MyFile.exe
```  

L’heure de commande suivante horodate un fichier à l’aide d’un serveur d’horodatage RFC 3161.  
  
```console  
signtool timestamp /tr http://timestamp.digicert.com /td SHA256 MyFile.exe
```  
  
 La commande suivante vérifie qu'un fichier a été signé.  
  
```console  
signtool verify MyFile.exe  
```  
  
 La commande suivante vérifie un fichier système qui a peut-être été signé dans un catalogue.  
  
```console  
signtool verify /a SystemFile.dll  
```  
  
 La commande suivante vérifie un fichier système qui est signé dans un catalogue nommé `MyCatalog.cat`.  
  
```console  
signtool verify /c MyCatalog.cat SystemFile.dll  
```  
