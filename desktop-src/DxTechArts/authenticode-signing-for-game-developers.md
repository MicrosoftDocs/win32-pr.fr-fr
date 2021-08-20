---
title: Signature Authenticode pour les développeurs de jeux
description: Cet article explique comment prendre en main l’authentification de votre jeu et comment intégrer l’authentification dans un processus de génération quotidien.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e41d9b0f1149394e1aa2634f5df2a428630bfc0e7bd006e86065567e28eb6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650429"
---
# <a name="authenticode-signing-for-game-developers"></a>Signature Authenticode pour les développeurs de jeux

L’authentification des données est de plus en plus importante pour les développeurs de jeux. Windows Vista et Windows 7 ont un certain nombre de fonctionnalités, telles que les contrôles de contrôle parental, qui requièrent que les jeux soient correctement signés pour s’assurer que personne n’a falsifié les données. Microsoft Authenticode permet aux utilisateurs finaux et au système d’exploitation de vérifier que le code du programme provient du propriétaire légitime et qu’il n’a pas été altéré ou endommagé de manière malveillante. Cet article explique comment prendre en main l’authentification de votre jeu et comment intégrer l’authentification dans un processus de génération quotidien.

-   [Contexte](#background)
-   [Prise en main](#getting-started)
-   [Utilisation d’une autorité de certification approuvée](#using-a-trusted-certificate-authority)
-   [Exemple d’utilisation d’un certificat de test](#example-using-a-test-certificate)
-   [Intégration de code signing dans le système de génération quotidien](#integrating-code-signing-into-the-daily-build-system)
-   [Révocation](#revocation)
-   [Pilotes de signature de code](#code-signing-drivers)
-   [Résumé](#summary)
-   [Plus d’informations](#more-information)

> [!Note]  
> depuis le 1er janvier 2016, Windows 7 et versions ultérieures n’approuvent plus de certificat de signature de code SHA-1 avec une date d’expiration du 1er janvier 2016 ou version ultérieure. pour plus d’informations, consultez [Windows l’application de la signature de Code Authenticode et](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) de l’horodatage.

 

## <a name="background"></a>Arrière-plan

Les certificats numériques sont utilisés pour établir l’identité de l’auteur. Les certificats numériques sont émis par un tiers approuvé, connu sous le nom d’autorité de certification, comme VeriSign ou Thawte. L’autorité de certification est chargée de vérifier que le propriétaire ne prétend pas une fausse identification. Après l’application à une autorité de certification pour un certificat, les développeurs commerciaux peuvent attendre une réponse à leur application en moins de deux semaines.

Une fois que l’autorité de certification a décidé que vous répondez à ses critères de stratégie, elle génère un certificat de signature de code conforme à X. 509, le format de certificat standard créé par l’Union internationale des télécommunications, avec les extensions de la version 3. Ce certificat vous identifie et contient votre clé publique. Elle est stockée par l’autorité de certification à des fins de référence, et une copie vous est fournie par voie électronique. En même temps, vous créez également une clé privée, que vous devez conserver en toute sécurité et que vous ne devez pas partager avec quiconque, même l’autorité de certification.

Une fois que vous disposez d’une clé publique et d’une clé privée, vous pouvez commencer à distribuer le logiciel signé. Microsoft fournit des outils pour effectuer cette opération dans le SDK Windows. Les outils utilisent un hachage unidirectionnel, produisent un condensé de longueur fixe et génèrent une signature chiffrée avec une clé privée. Ils combinent ensuite cette signature chiffrée avec votre certificat et vos informations d’identification dans une structure appelée bloc de signature et l’incorpore dans le format de fichier de l’exécutable. Tout type de fichier binaire exécutable peut être signé, y compris les dll, les fichiers exécutables et les fichiers CAB.

La signature peut être vérifiée de plusieurs façons. Les programmes peuvent appeler la fonction CertVerifyCertificateChainPolicy, et SignTool (signtool.exe) peut être utilisé pour vérifier une signature à partir de l’invite de ligne de commande. Windows L’Explorateur possède également un onglet signatures numériques dans Propriétés du fichier qui affiche chaque certificat d’un fichier binaire signé. (L’onglet signatures numériques s’affiche uniquement dans les propriétés de fichier des fichiers signés.) En outre, une application peut être vérifiée automatiquement à l’aide de [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

la signature Authenticode n’est pas seulement utile pour l’authentification des données par les utilisateurs finaux, mais elle est également nécessaire pour la mise à jour corrective de comptes d’utilisateurs limités et par les contrôles parentaux dans Windows Vista et Windows 7. en outre, les technologies futures dans Windows systèmes d’exploitation peuvent également nécessiter que le code soit signé. il est donc vivement recommandé que tous les développeurs professionnels et amateurs acquièrent un certificat de signature de code d’une autorité de certification. Pour plus d’informations sur cette opération, consultez [l’article utilisation d’une autorité de certification approuvée](#using-a-trusted-certificate-authority)plus loin dans cet article.

Le code de jeu, les répartiteurs et les programmes d’installation peuvent tirer parti de la signature Authenticode en vérifiant que les fichiers sont authentiques dans le code. Cela peut être utilisé pour la sécurité réseau générale et anti-fraude. Vous trouverez un exemple de code pour vérifier si un fichier est signé ici : [exemple de programme C : la vérification de la signature d’un fichier PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)et un exemple de code pour vérifier la propriété d’un certificat de signature sur un fichier signé sont disponibles ici : [obtention d’informations à partir des exécutables signés par Authenticode](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Mise en route

pour commencer, Microsoft fournit des outils avec Visual Studio 2005 et Visual Studio 2008, et dans le [SDK Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx), pour vous aider à effectuer et à vérifier le processus de signature de code. après l’installation de Visual Studio ou de l’SDK Windows, les outils décrits dans cet article technique se trouvent dans un sous-répertoire de l’installation de, qui peut inclure un ou plusieurs des éléments suivants :

-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ SDK \\ v 2.0 \\ Bin
-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ VC \\ PlatformSDK \\ Bin
-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 9,0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   % SystemDrive% \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 a \\ bin\\

Les outils suivants sont les plus utiles pour la signature de code :

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Outil de création de certificats (MakeCert.exe)
</dt> <dd>

Génère un certificat X. 509 de test, sous la forme d’un fichier. cer, qui contient votre clé publique et une clé privée, sous la forme d’un fichier. pvk. Ce certificat est destiné uniquement à des fins de test interne et ne peut pas être utilisé publiquement.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

crée un fichier de Exchange d’informations personnelles (. pfx) à partir d’une paire de fichiers. cer et. pvk. Le fichier. pfx contient vos clés publique et privée.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Signe le fichier à l’aide du fichier. pfx. SignTool prend en charge la signature des fichiers DLL, des fichiers exécutables, des fichiers Windows Installer (.msi) et des fichiers cab (.cab).

</dd> </dl>

> [!Note]  
> Lors de la lecture d’une autre documentation, vous pouvez trouver des références à SignCode (SignCode.exe), mais cet outil est déconseillé et n’est plus pris en charge ; utilisez SignTool à la place.

 

## <a name="using-a-trusted-certificate-authority"></a>Utilisation d’une autorité de certification approuvée

Pour obtenir un certificat approuvé, vous devez appliquer à une autorité de certification, telle que VeriSign ou Thawte. Microsoft ne recommande pas d’autorité de certification sur une autre, mais si vous souhaitez intégrer le service Rapport d’erreurs Windows (WER), vous devez envisager d’utiliser VeriSign pour émettre le certificat, car l’accès à la base de données WER requiert un compte WinQual qui nécessite un ID VeriSign. Pour obtenir la liste complète des autorités de certification tierces approuvées, consultez [membres du programme de certification racine de Microsoft](/previous-versions/ms995347(v=msdn.10)). pour plus d’informations sur l’inscription avec WER, consultez «[présentation de Rapport d’erreurs Windows](https://msdn.microsoft.com/)» dans la [Zone ISV](https://msdn.microsoft.com/).

Une fois que vous avez reçu votre certificat de l’autorité de certification, vous pouvez signer votre programme à l’aide de SignTool et publier votre programme au public. Toutefois, vous devez veiller à protéger votre clé privée, qui est contenue dans vos fichiers. pfx et. pvk. Veillez à conserver ces fichiers dans un emplacement sécurisé.

## <a name="example-using-a-test-certificate"></a>Exemple d’utilisation d’un certificat de test

Les étapes suivantes illustrent la création d’un certificat de signature de code à des fins de test, puis la signature d’un exemple de programme Direct3D (appelée BasicHLSL.exe) avec ce certificat de test. Cette procédure crée des fichiers. cer et. pvk, à savoir vos clés publiques et privées, respectivement, qui ne peuvent pas être utilisées pour la certification publique.

Dans cet exemple, un horodatage est également ajouté à la signature. Un horodatage empêche la signature de devenir non valide quand le certificat expire. Le code qui est signé mais qui n’a pas d’horodatage n’est pas validé après l’expiration du certificat. Par conséquent, tout le code publié publiquement doit avoir un horodatage.

**Pour créer un certificat et signer un programme**

1.  Créez un certificat de test et une clé privée à l’aide de l’outil de création de certificats (MakeCert.exe).

    L’exemple de ligne de commande suivant spécifie MyPrivateKey comme nom de fichier pour le fichier de clé privée (. pvk), MyPublicKey comme nom de fichier pour le fichier de certificat (. cer) et MySoftwareCompany comme nom du certificat. Elle rend également le certificat auto-signé, afin qu’il n’ait pas d’autorité racine non approuvée.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  créez un fichier de Exchange d’informations personnelles (. pfx) à partir de votre fichier de clé privée (. pvk) et du fichier de certificat (. cer) à l’aide de pvk2pfx.exe.

    Le fichier. pfx combine vos clés publiques et privées dans un fichier unique. L’exemple de ligne de commande suivant utilise les fichiers. pvk et. cer de l’étape précédente pour créer le fichier. pfx nommé MyPFX avec le mot de passe password \_ :

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  signez votre programme avec votre fichier de Exchange d’informations personnelles (. pfx) à l’aide de SignTool.

    Vous pouvez spécifier plusieurs options sur la ligne de commande. L’exemple de ligne de commande suivant utilise le fichier. pfx de l’étape précédente, attribue votre mot de passe \_ en tant que mot de passe, spécifie BasicHLSL comme fichier à signer et récupère un horodatage à partir d’un serveur spécifié :

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > L’URL du service d’horodatage est fournie par l’autorité de certification et est facultative pour le test. Il est important que la signature de production inclue une autorité d’horodatage valide ou que la signature ne parvienne pas à valider quand le certificat expire.

     

4.  Vérifiez que le programme est signé à l’aide de SignTool.

    L’exemple de ligne de commande suivant spécifie que SignTool doit tenter de vérifier la signature sur BasicHLSL.exe à l’aide de toutes les méthodes disponibles tout en fournissant une sortie détaillée :

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    Dans cet exemple, SignTool doit indiquer que le certificat est attaché, tout en indiquant également qu’il n’est pas approuvé, car il n’est pas émis par une autorité de certification.

5.  Approuvez le certificat de test.

    Pour les certificats de test, vous devez approuver le certificat. Cette étape doit être ignorée pour les certificats fournis par une autorité de certification, car ceux-ci sont approuvés par défaut.

    Sur les ordinateurs sur lesquels vous souhaitez approuver le certificat de test, exécutez la commande suivante :

    ```
    certmgr.msc
    ```

    

    Cliquez ensuite avec le bouton droit sur autorités de certification racines de confiance et choisissez toutes les tâches \| Importer. Ensuite, accédez au fichier. pfx que vous avez créé et suivez les étapes de l’Assistant, en plaçant le certificat dans les autorités de certification racines de confiance.

    Une fois l’Assistant terminé, vous pouvez commencer le test avec le certificat approuvé sur cet ordinateur.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Intégration de code signing dans le système de génération quotidien

Pour intégrer la signature du code à un projet, vous pouvez créer un fichier de commandes ou un script pour exécuter les outils en ligne de commande. Une fois le projet généré, exécutez SignTool avec les paramètres appropriés (comme indiqué à l’étape 3 de notre exemple).

Soyez particulièrement vigilant dans votre processus de génération pour vous assurer que l’accès aux fichiers. pfx et. pvk est limité à autant d’ordinateurs et d’utilisateurs que possible. En guise de meilleure pratique, les développeurs doivent uniquement signer le code à l’aide du certificat de test jusqu’à ce qu’ils soient prêts à être expédiés. Là encore, la clé privée (. pvk) doit être conservée dans un emplacement sécurisé, comme une salle sécurisée ou verrouillée, et idéalement sur un appareil de chiffrement, comme une carte à puce.

une autre couche de protection est fournie à l’aide de Microsoft Authenticode pour signer le package Windows Installer (MSI) lui-même. Cela permet de protéger le package MSI contre la falsification et l’endommagement accidentel. Pour plus d’informations sur la façon de signer des packages avec Authenticode, reportez-vous à la documentation de votre outil de création MSI.

## <a name="revocation"></a>Révocation

Si la sécurité de la clé privée est compromise ou si un événement lié à la sécurité rend un certificat Code-Signing non valide, le développeur doit révoquer le certificat. Cela affaiblirait l’intégrité du développeur et l’efficacité de la signature du code. Une autorité de certification peut également émettre une révocation avec une heure spécifique. le code signé avec un horodatage avant l’heure de révocation sera toujours considéré comme valide, mais le code avec un horodatage ultérieur sera non valide. La révocation de certificat affecte le code dans toutes les applications signées avec le certificat révoqué.

## <a name="code-signing-drivers"></a>Pilotes Code-Signing

Les pilotes peuvent et doivent être signés par Authenticode. les pilotes en mode noyau ont des exigences supplémentaires : les éditions 64 bits de Windows Vista et Windows 7 empêcheront l’installation de tous les pilotes non signés en mode noyau, et toutes les versions de Windows présenteront une invite d’avertissement lorsqu’un utilisateur tente d’installer un pilote non signé. en outre, les administrateurs peuvent définir stratégie de groupe pour empêcher l’installation de pilotes non signés sur Microsoft Windows Server 2003, Windows XP Professional édition x64 et les éditions 32 bits de Windows Vista et Windows 7.

de nombreux types de pilotes peuvent être signés avec une signature approuvée par Microsoft, dans le cadre du programme de Certification Windows de [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) ou du [programme de signature non classifié](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (anciennement signature de fiabilité du pilote), qui permet au système de faire confiance à ces pilotes et de les installer même sans informations d’identification d’administration.

au minimum, les pilotes doivent être signés par Authenticode, car les pilotes non signés ou auto-signés (c’est-à-dire, signés avec un certificat de test) ne peuvent pas être installés sur de nombreuses plateformes basées sur Windows. pour plus d’informations sur la signature des pilotes et du code et des fonctionnalités associées, consultez [configuration requise pour la signature des pilotes pour Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) sur [Windows Hardware developer Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Récapitulatif

L’utilisation de Microsoft Authenticode est un processus simple. Une fois que vous avez obtenu une région d’exécution limitée et créé une clé privée, il est simple d’utiliser les outils fournis par Microsoft. vous pouvez ensuite activer des fonctionnalités importantes dans Windows Vista et Windows 7, telles que le contrôle parental, et informer les clients que votre produit provient directement de son propriétaire légitime.

## <a name="more-information"></a>Plus d’informations

Pour plus d’informations sur les outils et les processus liés à la signature de code, consultez les liens suivants :

-   [Outils de chiffrement](/windows/desktop/SecCrypto/cryptography-tools)
-   [Informations de référence sur les outils API crypto](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Vue d’ensemble d’Authenticode et turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificats numériques](/windows/desktop/SecCrypto/digital-certificates)
-   [Déploiement d’Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Comment : créer des certificats temporaires à utiliser pendant le développement](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
