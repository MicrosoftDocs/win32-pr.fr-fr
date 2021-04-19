---
title: Programme d’application de bureau Windows
description: Vous pouvez obtenir des rapports d’analyse et des données de télémétrie détaillés qui vous permettent de voir comment fonctionnent vos applications de bureau Windows par le biais du nouveau programme d’application de bureau Windows.
ms.assetid: F1ED72A5-E1CD-4924-A81B-ED6FAF5E2AA3
ms.topic: article
ms.date: 11/02/2018
ms.openlocfilehash: 63fd252f7d98c6b7a401f6626f30dcdcd6751def
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314842"
---
# <a name="windows-desktop-application-program"></a>Programme d’application de bureau Windows

Vous pouvez obtenir des rapports d’analyse et des données de télémétrie détaillés qui vous permettent de voir comment fonctionnent vos applications de bureau Windows par le biais du nouveau programme d’application de bureau Windows.

Il n’y a aucun frais pour accéder à ces données. il vous suffit de vous [inscrire](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3deJsPaLaK4fU55nKvN21CjU6FsdJ0aPGfhsjGAZ0HR9bE6rgwHHX4izvRt_w-0VUlIF0ClCya4cVY6Uv4qTAqDrH8LTwFpjFGWVW2BAIJmAAuxBLZGTPS_DYy0wwgvTh1orWTCMvBdlOu_kF8vwNe4mjtk9JRMvYaETyspKrJi-s5Z2K7lKIPqnlFkwSU-aoot-3NxTeQ0wu6_RJ1nf_kLFatEkVAqokDSYTKkpv7zF6gA3YYriMFoC9_f2uxuXpI-STckg&nonce=637177463062493881.YjhiOTZjYTMtOTVhZS00OGM1LWI4MDItNWE5MThjMjA1ZjZmMTAyZDRiMGQtMDJhNC00ZDJmLWFkM2QtM2FjZDJkNjcxYWQy&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) et d’accepter le contrat de programme de l' [application de bureau Windows](https://go.microsoft.com/fwlink/?linkid=853677), puis de charger un fichier signé à l’aide du certificat que vous avez utilisé pour signer les fichiers exécutables de votre application.

## <a name="join-the-windows-desktop-application-program"></a>Rejoindre le programme d’application de bureau Windows

**Si votre société dispose déjà d’un compte de l’espace partenaires**: Connectez-vous à votre compte espace partenaires (à l’aide de la compte Microsoft associée au propriétaire du compte) et accédez à la page **programmes** (dans **paramètres du compte** ou en sélectionnant **tout** dans le menu de navigation gauche). Sous **programme d’application de bureau Windows**, cliquez sur **prise en main** pour rejoindre le programme sans coût supplémentaire. Si vous avez un locataire Azure AD associé à votre compte espace partenaires, les utilisateurs que vous avez ajoutés pourront accéder au programme d’application de bureau Windows. Bientôt, nous allons vous permettre de définir un accès plus granulaire pour ce programme.

> [!Tip]  
> Si votre entreprise dispose d’un compte espace partenaires, mais que vous n’y avez pas accès, demandez à votre administrateur de [vous ajouter en tant qu’utilisateur](/windows/uwp/publish/add-users-groups-and-azure-ad-applications). Notez que seul le propriétaire du compte peut rejoindre le programme d’application de bureau Windows.

 

**Si votre entreprise ne dispose pas d’un compte de l’espace partenaires**: vous pouvez vous inscrire gratuitement au [programme d’application de bureau Windows](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dWc5R_wIKVD0EbOy2UUxS0_0GQJnIAbD-eisMn7Gb4cJL18fRdelvbtj5_R0zoGlsebcnAxIvwKS5kx4Ma4mLMbU4l9ULsE9ajiZU4wtchLJXyJGsPCjCBUNV7TY1SzwXAI-LepSoXkqa8xSywVb7JZ3Xed-Lcw-kwEShFOwt0SdSdc1nNevHbPOhotOeFQcqbo0HESVYXk6pZORJ_OYimG99onp_zSTyludOvvaTd9GYKUgX9exCU5IHReP7MzJDHOgqTg&nonce=637177463071243612.NDU4MjE2ZTMtNmVkMi00YWNiLWEzZGEtMjYyNDRkODI0M2FmOTM3MmE1NzgtMzQ1OC00M2ZkLWJhMDktYzI4YTNhNzdiYTk0&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) . Prochainement, nous fournirons la possibilité d' [associer un locataire Azure ad à votre compte](/windows/uwp/publish/add-users-groups-and-azure-ad-applications) afin que d’autres personnes de votre entreprise puissent également se connecter.

## <a name="add-your-desktop-applications"></a>Ajouter vos applications de bureau

Une fois que vous avez rejoint le programme, vous devez ajouter vos applications de bureau Windows à votre tableau de bord afin de pouvoir commencer à afficher vos rapports d’analyse.

Nous utilisons la signature de code pour établir l’identité de votre entreprise et récupérer des analyses pour les applications que vous publiez.

Nous vous fournirons un fichier et vous demanderons de le signer avec les mêmes certificats de signature de code valides, non expirés et non révoqués que ceux que vous utilisez pour signer vos applications de bureau. Après cela, vous allez charger ce fichier signé dans votre tableau de bord. Cela nous permet de savoir que toutes les applications de bureau signées avec le même certificat appartiennent à votre compte. Nous n’utilisons pas vos informations de certificat à d’autres fins.

> [!Important]  
> Vous n’avez pas besoin de répéter ce processus si vous publiez une nouvelle application de bureau. Une fois que vous avez téléchargé le fichier signé, nous constatons automatiquement les nouvelles applications qui sont signées avec le même certificat, et nous récupérons automatiquement les analytiques pour ces produits. Vous n’avez pas non plus besoin de distribuer le fichier fourni dans vos applications ou d’envoyer un type de mappage pour vos produits

 

**Pour ajouter une ou plusieurs applications de bureau**

1.  À partir de votre tableau de bord, sélectionnez **Ajouter des applications de bureau**.
2.  Sur la page suivante, téléchargez le fichier signable en sélectionnant **Télécharger le fichier**, puis enregistrez le fichier sur votre ordinateur.
3.  Signez le fichier que vous venez de télécharger à l’aide du même certificat de signature de code que celui utilisé pour authentifier vos applications de bureau. Vous pouvez utiliser SignTool.exe (disponible dans Microsoft Visual Studio et dans le cadre de la [SDK Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk)) pour signer ce fichier. Pour plus d’informations sur ce processus, voir ci-dessous.
4.  Téléchargez le fichier que vous venez de signer en le faisant glisser vers le champ (ou cliquez pour parcourir vos fichiers).
5.  Sélectionnez **Envoyer** pour terminer le processus.

![étapes d’ajout d’applications de bureau](images/uploadcert.png)

Si vous utilisez plusieurs certificats de signature de code, vous pouvez répéter les étapes ci-dessus pour chacun de vos certificats. Vous pouvez télécharger, signer et charger un fichier pour chaque certificat actuel que vous utilisez pour signer vos applications. Toutefois, vous ne pouvez utiliser qu’un seul certificat par fichier téléchargé.

Une fois ces étapes terminées, nous allons identifier les applications de bureau Windows signées avec le même certificat que celui utilisé pour signer le fichier. Dans la plupart des cas, nous commençons à montrer des rapports analytiques dans un délai de 48 heures, bien que cela puisse parfois prendre un peu plus de temps.

## <a name="use-signtoolexe-to-sign-the-downloaded-file"></a>Utiliser signtool.exe pour signer le fichier téléchargé

Microsoft fournit un outil permettant de signer des fichiers, SignTool.exe, avec Visual Studio et dans le [SDK Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk). Vous pouvez utiliser cet outil pour exécuter et vérifier le processus de signature de code. Plus d’informations sur SignTool.exe sont disponibles [ici](/dotnet/framework/tools/signtool-exe).

Voici deux des façons les plus courantes d’utiliser cet outil pour signer le fichier signable.

-   Si vous avez accès au certificat de signature de code en tant que fichier d' [échange d’informations personnelles (pfx)](/windows-hardware/drivers/install/personal-information-exchange---pfx--files) :

    ``` syntax
    signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin
    ```

    ![Capture d’écran montrant une fenêtre d’invite de commandes affichant la commande’SignTool Sign/f MyCert. pfx/p MyCertPassword/v SignableFile. bin'.](images/signtool2.png)

-   Si le certificat de signature de code est disponible dans votre magasin de certificats local :

    ``` syntax
    Signtool sign /v /s MY /n CertSubjectName SignableFile.bin
    ```

    ![fenêtre d’invite de commandes qui affiche cette commande](images/signtool.png)

Une fois le fichier signé, vous pouvez vérifier qu’il a été correctement signé avec un certificat valide avec les éléments suivants :

``` syntax
signtool verify /a SignableFile.bin
```

## <a name="viewing-your-analytic-data"></a>Affichage de vos données analytiques

Une fois que vos fichiers signés ont été téléchargés et que nous avons identifié vos applications de bureau, votre tableau de bord présente une vue d’ensemble de vos applications, ainsi que des mesures clés.

Nos données de télémétrie affichent des informations d’intégrité telles que des blocages pour chaque application associée à votre certificat. Votre tableau de bord présente une vue d’ensemble de vos applications, ainsi que des mesures clés. Vous pouvez sélectionner n’importe quelle application pour afficher son [rapport d’intégrité](#health-report), [installer le rapport](#installs-report)et [bloquer](#application-blocks-report) le rapport dans le tableau de bord. Vous pouvez également [récupérer des données analytiques par programmation à l’aide de l’API Microsoft Store Analytics](#retrieve-analytic-data-using-the-microsoft-store-analytics-api).

> [!Note]  
> Si nous détectons que les métadonnées d’une application ont été mises à jour pour utiliser un nouveau nom, nous commençons à signaler les nouvelles données sous le nouveau nom. Les données d’historique associées à l’ancien nom seront conservées pendant 30 jours.
> 
> L’analyse ne sera pas disponible pour une application tant qu’elle n’a pas été installée sur au moins 100 appareils.


### <a name="health-report"></a>Rapport sur l’intégrité

Le rapport d' **intégrité** vous permet d’accéder aux données relatives aux performances et à la qualité de votre application, notamment aux incidents et aux événements qui ne répondent pas. Le cas échéant, vous pouvez afficher les traces de la pile et/ou les fichiers CAB pour un débogage supplémentaire.

![rapport d’intégrité-programme d’application de bureau Windows](images/health.png)

Vous pouvez filtrer les données de plusieurs façons, ce qui vous permet d’effectuer les opérations suivantes :

-   Afficher un résumé de tous les types d’échec, triés par nombre d’accès
-   Explorez une défaillance particulière et téléchargez des traces de pile pour déboguer le problème plus rapidement
-   Comparer une nouvelle version de votre application aux versions précédentes
-   Affichez les données d’intégrité dans l’agrégat ou par région, ce qui vous permet d’isoler les problèmes spécifiques à une région.
-   Comparer les performances de vos applications de bureau sur les différentes versions de Windows ou sur une version spécifique, telle que la dernière version de Windows 10
-   Afficher les informations d’intégrité d’un fichier exécutable particulier inclus dans votre application

Sélectionnez **charger les symboles** en haut de la table des **échecs** pour télécharger un fichier. zip contenant les [fichiers de symboles](/windows-hardware/drivers/debugger/symbols-and-symbol-files)de votre application. Ces fichiers de symboles seront indexés et utilisés pour produire des traces de pile plus précises. Les types de fichiers de symboles dans le fichier. zip doivent être. pdb,. dll ou. exe. Une fois que vous avez téléchargé correctement votre fichier. zip, vous devez en voir moins **! Valeurs inconnues** pour les nouveaux échecs dans la liste d’erreurs de votre application en 5 jours environ.

### <a name="installs-report"></a>Installe le rapport

Le rapport **installations** vous permet de voir le nombre d’appareils sur lesquels une application a été installée pour un jour donné et le nombre moyen d’appareils sur lesquels chaque version de l’application a été installée au cours des 30 derniers jours.

Vous pouvez filtrer les données de plusieurs façons, ce qui vous permet d’effectuer les opérations suivantes :

-   Afficher un résumé de vos installations, triées par popularité
-   Comparer une nouvelle version de votre application aux versions précédentes
-   Afficher les données d’installation dans l’agrégat ou par région
-   Comparer les performances de vos applications de bureau sur les versions de Windows ou sur une version spécifique, telle que la dernière version de Windows 10 ou les versions Windows Insider rapides et lentes

### <a name="application-blocks-report"></a>Rapport des blocs d’application

Le rapport **blocs d’application** vous permet d’afficher des informations sur les appareils Windows 10 sur lesquels votre application affecte les mises à niveau Windows 10. Vous pouvez voir le nombre d’appareils affectés à un jour donné, ainsi que le nombre moyen d’appareils au cours des 30 derniers jours.

Les types de blocs de mise à niveau inclus sont les suivants : 

<table>
<tr><th>Category</th><th>Problème</th><th>Description</th><th>Guide fourni aux utilisateurs</th></tr>
<tr><td>Sédiment potentiel</td><td>Bloquera la mise à niveau</td><td>L’application ne fonctionnera pas sur la nouvelle version du système d’exploitation. Une action de l’utilisateur est nécessaire lors de l’installation pour poursuivre la mise à niveau.</td><td>Supprimez l’application avant d’effectuer la mise à niveau et contactez le développeur pour obtenir une version compatible de l’application.</td></tr>
<tr><td>Sédiment temporaire</td><td>Risque de blocage de la mise à niveau. Vous devez tester l’application.</td><td>Microsoft examine les problèmes de mise à niveau liés à cette application. La mise à niveau ne sera pas déployée pour les utilisateurs qui peuvent être affectés.</td><td>Supprimez l’application avant d’effectuer la mise à niveau et contactez le développeur pour obtenir une version compatible de l’application.</td></tr>
<tr><td>Notification d’exécution</td><td>Peut ne pas fonctionner correctement dans la nouvelle version du système d’exploitation, mais ne bloque pas la mise à niveau</td><td>L’application n’empêchera pas la mise à niveau, mais des problèmes peuvent l’empêcher de fonctionner correctement dans la nouvelle version du système d’exploitation.</td><td>Aucune action n’est requise pour continuer la mise à niveau, mais veillez à tester l’application sur la nouvelle version du système d’exploitation et contactez le développeur pour obtenir une version compatible, si nécessaire.</td></tr>
</table>

### <a name="retrieve-analytic-data-using-the-microsoft-store-analytics-api"></a>Récupérer des données analytiques à l’aide de l’API Microsoft Store Analytics

L’API Microsoft Store Analytics vous permet de récupérer par programme des données analytiques pour les applications que vous avez ajoutées à votre compte.

Cette API offre les méthodes suivantes spécifiques au programme d’application de bureau Windows :

-   [Installe](/windows/uwp/monetize/get-desktop-app-installs)
-   [Échecs d’accès](/windows/uwp/monetize/get-desktop-application-error-reporting-data)
-   [Détails de l’échec](/windows/uwp/monetize/get-details-for-an-error-in-your-desktop-application)
-   [Arborescence des appels de procédure](/windows/uwp/monetize/get-the-stack-trace-for-an-error-in-your-desktop-application)
-   [Fichier CAB](/windows/uwp/monetize/download-the-cab-file-for-an-error-in-your-desktop-application)
-   [Blocs de mise à niveau](/windows/uwp/monetize/get-desktop-block-data)
-   [Détails du bloc de mise à niveau](/windows/uwp/monetize/get-desktop-block-data-details)


Pour plus d’informations sur l’utilisation de cette API, consultez [accéder aux données analytiques à l’aide des services de magasin](/windows/uwp/monetize/access-analytics-data-using-windows-store-services).

## <a name="managing-your-desktop-application-metadata"></a>Gestion des métadonnées de vos applications de bureau

Nous utilisons les métadonnées nom du fichier, version du fichier, nom du produit et version du produit dans vos fichiers exécutables pour déduire les regroupements logiques de fichiers exécutables en applications. Si les fichiers exécutables n’ont pas de métadonnées exactes, ils peuvent apparaître ensemble sous un nom d’application **inconnu** , ou le nom de l’application prend par défaut le nom de l’exécutable individuel.

En gardant à jour les métadonnées de vos applications et fichiers, assurez-vous qu’ils sont représentés correctement dans votre tableau de bord. Voici quelques recommandations :

-   Utilisez votre certificat pour signer chaque fichier exécutable que vous souhaitez afficher dans votre rapport d’analyse, et non uniquement vos exécutables d’installation.
-   Fournir un nom de produit cohérent et des informations de version de produit pour tous les fichiers exécutables qui appartiennent à la même application (par exemple, *mon application*). Si certains de vos fichiers exécutables sont distribués avec plusieurs applications, donnez-leur des noms uniques (c’est-à-dire des *composants partagés*) afin de pouvoir afficher les analyses de ces fichiers exécutables séparément des applications avec lesquelles ils ont été distribués.
-   Chaque fois que vous apportez des modifications à vos métadonnées, vous pouvez voir une nouvelle entrée pour votre application dans votre tableau de bord. Si vous apportez une modification, les nouvelles données de télémétrie entrantes reflètent vos modifications, mais vos anciennes données de télémétrie s’affichent toujours comme une application **inconnue** .
-   Lorsque vous modifiez un fichier, veillez à mettre à jour la version de l’application et les numéros de version du produit.
    > [!Tip]  
    > Utilisez les ressources [**VERSIONINFO**](/windows/desktop/menurc/versioninfo-resource) pour définir **FileDescription**, **FileVersion**, **ProductName** et **ProductVersion** pour vos fichiers et applications. L’exemple suivant définit une ressource **VERSIONINFO** :
    >
    > ``` syntax
    > #define VER_PRODUCTNAME_STR      "Sample App"
    > #define VER_PRODUCTVERSION       3,10,349,0
    > #define VER_PRODUCTVERSION_STR   "3.10.349.0\0"
    > #define VER_FILEDESCRIPTION_STR  "Sample File"
    > #define VER_FILEVERSION          3,10,349,0
    > #define VER_FILEVERSION_STR      "3.10.349.0\0"
    > #define VER_COMPANYNAME_STR     "XYZ Corp."
    > #define VER_LEGALCOPYRIGHT_STR   "Copyright \251 XYZ Corp." 
    >  
    > VS_VERSION_INFO VERSIONINFO
    > FILEVERSION VER_FILEVERSION
    > PRODUCTVERSION VER_PRODUCTVERSION
    > FILEFLAGSMASK VER_FILEFLAGSMASK
    > FILEFLAGS VER_FILEFLAGS
    > FILEOS VER_FILEOS
    > FILETYPE VER_FILETYPE
    > FILESUBTYPE VER_FILESUBTYPE
    > BEGIN
    >     BLOCK "StringFileInfo"
    >     BEGIN
    >         BLOCK "040904E4"
    >         BEGIN
    >             VALUE "ProductName",      VER_PRODUCTNAME_STR
    >             VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
    >             VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
    >             VALUE "FileVersion",      VER_FILEVERSION_STR
    >             VALUE "CompanyName",      VER_COMPANYNAME_STR
    >             VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
    >         END
    >     END
    >      
    > END 
    > ```

     

## <a name="add-and-manage-account-users"></a>Ajouter et gérer des utilisateurs du compte

Vous pouvez utiliser Azure Active Directory pour ajouter et gérer des utilisateurs supplémentaires dans votre compte de programme d’application de bureau Windows. Vous pouvez ajouter des utilisateurs, des groupes d’utilisateurs ou des applications Azure AD, en attribuant à chacun un rôle prédéfini (responsable ou développeur).

### <a name="associate-azure-active-directory-with-your-account"></a>Associer Azure Active Directory à votre compte

Pour pouvoir ajouter et gérer des utilisateurs de comptes, vous devez d’abord associer votre compte aux Azure Active Directory de votre organisation. Si votre organisation utilise déjà Office 365 ou d’autres services professionnels de Microsoft, vous disposez déjà d’Azure AD. Dans le cas contraire, vous pouvez créer un nouveau Azure AD locataire sans frais supplémentaires.

Pour plus d’informations, consultez [associer des Azure Active Directory à votre compte espace partenaires](/windows/uwp/publish/associate-azure-ad-with-dev-center) . Bien que la rubrique se concentre sur le programme Windows Apps Developer, l’Association d’un locataire fonctionne de la même façon pour le programme d’application de bureau Windows.

### <a name="add-users-groups-and-azure-ad-applications-to-your-account"></a>Ajouter des utilisateurs, des groupes et des applications de Azure AD à votre compte

Une fois que vous avez configuré l’Association Azure AD, vous pouvez ajouter des utilisateurs en accédant à la section utilisateurs sous paramètres du compte. Chaque utilisateur se voit attribuer un rôle qui définit son accès au compte. Vous pouvez également ajouter des groupes d’utilisateurs et des applications de Azure AD pour leur accorder l’accès à votre compte espace partenaires. Pour plus d’informations sur l’ajout d’utilisateurs, voir [Ajouter des utilisateurs, des groupes et des applications de Azure ad](/windows/uwp/publish/add-users-groups-and-azure-ad-applications).

Chaque utilisateur, groupe ou Azure AD application que vous ajoutez à votre compte doit se voir attribuer un rôle. Ce processus est décrit dans [définir des rôles ou des autorisations personnalisées pour les utilisateurs du compte](/windows/uwp/publish/set-custom-permissions-for-account-users). Toutefois, Notez que pour le programme d’application de bureau Windows, il n’est pas possible d’attribuer des autorisations personnalisées ou de restreindre l’accès par produit. Au lieu de cela, chaque utilisateur doit se voir attribuer l’un des rôles standard suivants.



| Rôle      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manager   | Peut télécharger et supprimer des certificats et afficher toutes les données analytiques. Dispose d’un accès complet au compte, à l’exception de la modification des informations financières. Cela comprend la gestion des utilisateurs, mais notez que la possibilité de créer et de supprimer des utilisateurs dans le locataire Azure AD dépend de l’autorisation du compte dans Azure AD. Autrement dit, si un utilisateur se voit attribuer le rôle de responsable, mais ne dispose pas des autorisations d’administrateur général dans le Azure AD de l’organisation, il ne peut pas créer de nouveaux utilisateurs ou supprimer des utilisateurs de l’annuaire (même s’ils peuvent modifier le rôle de compte d’un utilisateur).<br/> Notez que si votre compte est associé à plusieurs Azure AD locataires, un gestionnaire ne peut pas voir les détails complets d’un utilisateur (y compris le prénom, le nom, le message de récupération du mot de passe et s’il s’agit d’un administrateur général Azure AD), sauf s’ils sont connectés au même locataire que cet utilisateur avec un compte disposant d’autorisations d’administrateur général pour ce locataire. Toutefois, ils peuvent ajouter et supprimer des utilisateurs dans n’importe quel client associé au compte. <br/> |
| Développeur | Peut afficher les applications et les détails du certificat associés au compte et peut afficher le rapport **intégrité** et **installation** . Impossible d’afficher les informations financières ou les paramètres du compte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="faq"></a>Questions fréquentes (FAQ)

-   **Pourquoi ne puis-je pas voir les données d’une application ?** Nous n’affichons pas les données tant que vous n’avez pas détecté suffisamment d’utilisateurs pour collecter des informations significatives. Si vous venez de publier votre application, il peut être nécessaire de prendre un certain temps pour atteindre ce seuil d’adoption minimal. Une autre raison pour laquelle vous risquez de ne pas voir les données est si vous n’avez pas signé de fichier avec le certificat pour une certaine application. Veillez à charger les fichiers signés avec chaque certificat que vous utilisez pour signer vos applications.
-   **Puis-je accéder à ces données par le biais d’une API ?** Oui, les données sont rendues disponibles par le biais d’une API publique lorsque le programme est disponible pour tous les développeurs.
-   **Qu’en est-il des applications avec des certificats anciens ?** Malheureusement, nous ne prenons pas en charge l’envoi de certificats expirés ou révoqués, même si vous les renouvelez avec la même clé.
-   **Pourquoi vois-je une application que je ne reconnais pas ?** Si le certificat que vous utilisez pour signer des fichiers dans votre application est également utilisé par une autre personne de votre entreprise pour signer une autre application, vous verrez également des données de télémétrie pour cette application. À l’avenir, nous fournirons une option pour masquer les applications de votre tableau de bord. Si votre compte d’entreprise est associé à un locataire Azure AD, vous pouvez demander à votre administrateur de modifier les autorisations utilisateur afin que seules des applications spécifiques soient visibles.
-   **Comment puis-je fournir des commentaires sur l’expérience ou obtenir de l’aide ?** Si vous avez besoin d’aide, vous pouvez créer une demande de support [ici](https://developer.microsoft.com/windows/support/). Pour partager vos commentaires, utilisez le lien de **Commentaires** (sous **paramètres du compte**) et sélectionnez la zone **analytique** pour nous faire part de votre opinion. 
 

