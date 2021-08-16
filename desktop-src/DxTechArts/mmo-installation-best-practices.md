---
title: Meilleures pratiques pour l’installation de jeux en ligne massivement multijoueurs
description: cet article décrit la création d’une chaîne de conception de confiance pour l’installation du client de jeux en ligne massivement multijoueurs (MMOG) et les systèmes de mise à jour de jeux personnalisés qui fonctionnent bien avec Windows et le modèle de sécurité de Windows Vista et Windows 7.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b574bdf2ae98b28fabed97340d6aa38b1a864c24519bb6532d0aa4069882efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815433"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Meilleures pratiques pour l’installation de jeux en ligne massivement multijoueurs

cet article décrit la création d’une chaîne de conception de confiance pour l’installation du client de jeux en ligne massivement multijoueurs (MMOG) et les systèmes de mise à jour de jeux personnalisés qui fonctionnent bien avec Windows et le modèle de sécurité de Windows Vista et Windows 7. L’approche est conçue pour activer la mise à jour corrective des titres MMOG tout en prenant en charge les comptes d’utilisateur standard, qui ont un accès limité au disque dur et au registre système.

-   [Pourquoi les clients MMOG ont des exigences différentes pour les jeux achetés au détail traditionnels](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Vue d’ensemble d’une approche de chaîne d’approbation](#overview-of-a-chain-of-trust-approach)
-   [Tout est validé sur le serveur, pourquoi dois-je m’inquiéter si mon client est piraté ?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Construction de l’application Trust-Worthy Loader](#construction-of-the-trust-worthy-loader-application)
    -   [Lecture en arrière-plan](#background-reading)
    -   [Installation du chargeur approuvé et Patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [Installation des exécutables, des dll et des données du jeu](#installation-of-the-game-executables-dlls-and-data)
    -   [Code de modification de la liste de Access Control](#access-control-list-modification-code)
    -   [Installations pour les utilisateurs expérimentés](#installations-for-advanced-users)
    -   [Vérification de l’approbation du chargeur](#the-loaders-verification-of-trust)
    -   [Validation des données](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Pourquoi les clients MMOG ont des exigences différentes pour les jeux achetés au détail traditionnels

La nature constamment connectée et en constante évolution de MMOG en fait une exigence fondamentale pour fournir des mises à jour régulières du code client et du contenu pour corriger les failles de sécurité et étendre l’expérience de jeu. Avec le potentiel des mises à jour presque quotidiennes, le scénario MMOG nécessite une gestion attentive pour garantir une expérience utilisateur conviviale. Cela diffère du modèle d’achat de vente au détail traditionnel où un petit nombre de correctifs peuvent être fournis à proximité de la date d’expédition du produit. la Windows Installer technologie limitée de mise à jour des utilisateurs fournie avec le système d’exploitation est conçue pour gérer un petit nombre de correctifs d’application, et non pas la grande quantité et la fréquence élevée requises par mmog. C’est pourquoi il est souvent nécessaire de développer des systèmes de correctifs personnalisés pour répondre aux besoins des MMOG, y compris les exigences particulières spécifiques au MMOG en cours de développement.

étant donné que de nombreux ordinateurs sont connectés à Internet, Windows Vista et Windows 7 ont des restrictions et des protections de sécurité plus strictes pour les utilisateurs, qui limitent l’accès des applications aux différentes zones du disque dur. contrairement à Windows XP, ces restrictions sont activées pour le mode par défaut pour les comptes d’utilisateur. Ces restrictions doivent être prises en compte lors de la conception de la disposition d’un jeu, d’un fichier exécutable et de données, ainsi que du système de mise à jour qui lui est associé. Pour plus d’informations sur les mesures de sécurité fournies par le système d’exploitation, consultez [contrôle de compte d’utilisateur pour les développeurs de jeux](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

## <a name="overview-of-a-chain-of-trust-approach"></a>Vue d’ensemble d’une approche de chaîne d’approbation

L’approche de mise à jour personnalisée présentée dans ce livre blanc repose sur la présence d’une application de chargeur fiable installée dans le dossier Program Files protégé tout en conservant les fichiers et les données exécutables du jeu dans une zone partagée All-User accessible. Une chaîne d’approbation commence par le chargeur qui effectue des vérifications de validité sur les fichiers binaires et les données de jeu avant le lancement.

![la chaîne d’approbation commence par un chargeur fiable](images/mmo-installation-best-practices-01.gif)

Le chargeur de confiance doit avoir suffisamment de logique pour être en mesure de vérifier que l’exécutable du jeu et les autres binaires n’ont pas été falsifiés avant de lancer le jeu. Le chargeur peut également vérifier les données de jeu aussi souvent que nécessaire. Toutefois, la taille des données de jeu est généralement trop importante pour permettre une vérification à chaque fois en une seule passe. Une autre approche consiste à utiliser un modèle d’échantillonnage qui garantit que la vérification de l’ensemble du jeu de données se produit sur une période prolongée. L’application Loader peut contenir un moteur de mise à jour de jeu, qui offre une méthode fiable pour intégrer les mises à jour au jeu installé.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Tout est validé sur le serveur, pourquoi dois-je m’inquiéter si mon client est piraté ?

Il est impossible de faire confiance au fait que le client n’a pas été compromis ; par conséquent, il est courant pour les serveurs MMOG de valider toutes les données reçues du client. Alors que ce traitement peut identifier les clients de jeux compromis ou tricher au sein de l’univers du jeu, le serveur ne peut pas identifier facilement tous les problèmes auxquels le client du jeu peut être exposé. Il est important de renforcer la protection contre les pirates qui souhaitent utiliser votre client comme une plateforme pour les attaques sur votre service, d’autres utilisateurs, ou encore simplement comme un vecteur pour attaquer les ordinateurs clients eux-mêmes. L’application de la signature de code et des techniques de vérification des données peut aider à détecter les clients compromis avant qu’ils ne soient exécutés. Étant donné que le mécanisme de mise à jour corrective nécessite l’exposition d’exécutables et de fichiers binaires DLL qui ne sont pas protégés par les autorisations de lecture seule standard sur les fichiers programme, la validation de ces fichiers avant leur lancement est importante pour la sécurité globale du système.

Ce modèle ne tente pas de traiter le scénario d’utilisateur administrateur malveillant dans lequel le chargeur lui-même peut devenir compromis, mais se concentre sur la protection des utilisateurs standard contre l’exécution accidentelle de code falsifié. Les techniques de validation serveur traditionnelles sont en fait la seule solution d’atténuation possible pour les administrateurs système de clients malveillants.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Construction de l’application Trust-Worthy Loader

### <a name="background-reading"></a>Lecture en arrière-plan

Les lecteurs doivent se familiariser avec la documentation suivante, qui fournit des détails sur la technologie de base pour s’assurer de la meilleure pratique en matière de confiance basée sur les logiciels.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Signature du code
</dt> <dd>

[Signature Authenticode pour les développeurs de jeux](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) sur MSDN

</dd> </dl>

La section suivante détaille les API qui doivent être utilisées pour construire l’application Loader, qui prend en charge la disposition des disques pour l’installation et la vérification de la vérification de l’approbation.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Installation du chargeur approuvé et Patcher

Le chargeur approuvé et la version de base de l’utilitaire patcher doivent être installés sous le dossier Program Files protégé sur le disque dur, comme dans les installations traditionnelles. l’Installation et la mise à jour corrective de l’application loader requièrent des droits d’administrateur. il est donc important de réduire la fréquence de mise à jour du chargeur pour s’assurer que les utilisateurs finaux n’ont pas besoin d’élever souvent les privilèges, bien que Windows Installer une mise à jour corrective de l’utilisateur limité puisse être utilisée pour éviter l’élévation des correctifs du chargeur.

consultez l’article correctif logiciel du jeu dans Windows XP, Windows Vista et Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Installation des exécutables, des dll et des données du jeu

Pour faciliter les mises à jour de l’utilisateur standard du jeu sans privilège administratif, l’exécutable, les dll et les données des jeux doivent être installés dans une zone du disque dur accessible en écriture pour tous les utilisateurs. Le système d’exploitation fournit une zone « toutes les données d’application » qui peut être utilisée comme emplacement par défaut pour l’installation. [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) doit être utilisé avec la \_ clé common \_ AppData de CSIDL pour déterminer le chemin d’accès de fichier pour cette zone. Il est important de ne pas faire d’hypothèses sur le chemin d’accès vers lequel cette clé est retournée, car elle peut être configurée par l’utilisateur.

L’installation doit modifier ou gérer les autorisations de dossier afin d’obtenir l’accès en écriture tout-utilisateur-partagé nécessaire pour mettre à jour le titre. Avec les autorisations adéquates, la fonctionnalité de mise à jour de jeu du programme Loader peut facilement corriger le jeu sans avoir besoin de privilèges spéciaux de tout compte d’utilisateur, y compris les heures de lancement par les utilisateurs standard.

### <a name="access-control-list-modification-code"></a>Code de modification de la liste de Access Control

pour Windows XP, vous devrez exécuter du code pour modifier manuellement la liste de contrôle d’accès (ACL). voici un exemple de fonction qui montre comment procéder :

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

cet exemple de code fonctionne également pour Windows Vista et Windows 7 ; Toutefois, ils fournissent également à l’utilitaire de ligne de commande icacls la possibilité de modifier les listes de contrôle d’accès des fichiers que vous pouvez choisir d’utiliser à la place.

L’outil fournit une aide détaillée lorsqu’il est exécuté, mais un exemple d’utilisation de l’outil est :

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Cette utilisation permet d’octroyer les autorisations de suppression et d’écriture DAC à l’utilisateur sur le dossier de jeu stocké dans les zones tous les utilisateurs du disque dur.

### <a name="installations-for-advanced-users"></a>Installations pour les utilisateurs expérimentés

Pour les scénarios d’installation utilisateur avancés, un utilisateur peut souhaiter spécifier manuellement le chemin d’installation des jeux. La sélection de répertoire doit être limitée à une partie externe des fichiers programme pour garantir que le dossier se trouve dans une zone véritablement partageable du disque dur. Le chemin d’accès sélectionné par l’utilisateur ne doit être utilisé que pour les fichiers et les fichiers exe des jeux, car le chargeur de jeux et les fichiers exe patcher doivent toujours être installés dans le dossier des fichiers de programme sécurisés pour une meilleure sécurité.

### <a name="the-loaders-verification-of-trust"></a>Vérification de l’approbation du chargeur

Windows fournit la fonction [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) pour vérifier la validité du code signé et est basée sur les services de chiffrement du système d’exploitation. La fonction est entièrement documentée sur la fonction MSDN : **WinVerifyTrust** .

L’exemple de programme suivant sur MSDN détaille l’utilisation de la fonction pour déterminer si un exécutable de programme est signé avec un certificat valide : [exemple de programme C : vérification de la signature d’un fichier PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file).

Dans le but de vérifier que l’exécutable du jeu signé est digne de confiance pour être exécuté à partir du chargeur, l’action de vérification générique suffit :

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

\_Vérification générique de l’action WINTRUST \_ \_ \_ v2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>C.-à-d
</dt> <dd>

Vérifiez un fichier ou un objet à l’aide du fournisseur de stratégie Authenticode.

</dd> </dl>

La fonction accepte un argument de structure d’entrée qui contient des informations dont le fournisseur d’approbation a besoin pour traiter l’action spécifiée. En général, comme dans le cas de l’exemple précédent, la structure contient des informations qui identifient l’objet que le fournisseur d’approbation doit évaluer.

Le format de la structure est spécifique à l’identificateur d’action. La rubrique suivante sur MSDN détaille l’exemple de structure pour le fournisseur WinTrust : structure de [**\_ données wintrust**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) .

Si le fournisseur d’approbation vérifie que le sujet est approuvé pour l’action spécifiée, la valeur de retour est zéro. Aucune autre valeur, hormis zéro, ne doit être considérée comme un retour correct.

### <a name="data-validation"></a>Validation des données

le mécanisme de coconception prend uniquement en charge la signature de quelques types de fichiers spécifiques, y compris les fichiers exécutables, les dll, les packages de Windows Installer (fichiers .msi) et les fichiers cab (.cab). L’API [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) ne doit pas être utilisée pour vérifier que les fichiers de données volumineux (fichiers .cab, par exemple) n’ont pas été falsifiés, car il existe des problèmes de performances et de stabilité lors de la validation de fichiers volumineux. Les exécutables de programme tendent à être suffisamment petits pour une vérification de confiance totale à l’aide du fournisseur WinTrust, mais les fichiers de données pour les jeux sont souvent du domaine de plusieurs gigaoctets en taille. L’approche adoptée par le chargeur pour la vérification des données de jeu doit être celle où un petit échantillon du jeu de données est testé au moment de l’exécution du jeu. Cette approche répartit le coût des tests de vérification au cours de la durée de vie de l’expérience de jeu et peut fournir une expérience utilisateur transparente sans temps d’attente. Pour y parvenir, une organisation minutieuse des données peut être nécessaire. Certains MMOG utilisent une approche de base de données pour aider à gérer, gérer et vérifier l’exactitude des ressources de jeu au fil du temps.

Du point de vue de la sécurité, le code client doit être conçu pour ne pas faire confiance aux fichiers de données, même si vous utilisez un type de validation de données de base avec le chargeur approuvé. Les vérifications d’en-tête, les hachages et d’autres contrôles d’intégrité traditionnels doivent être utilisés. la sécurisation renforcée du code d’e/s du client doit également être effectuée à l’aide de techniques telles que le test de fuzzing et la possibilité de tirer parti des outils d’analyse de code statique automatique tels que le commutateur **/analyze** dans Visual Studio 2005 et Visual Studio 2008 (disponible dans Visual Studio Team System et le compilateur gratuit fourni avec le SDK Windows).

Pour plus d’informations sur la sécurité logicielle, consultez [meilleures pratiques en matière de sécurité dans le développement de jeux](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 