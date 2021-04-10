---
title: Déploiement de Direct3D 11 pour les développeurs de jeux
description: Cet article explique comment déployer les composants Direct3D 11 sur un système, si nécessaire.
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199332"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>Déploiement de Direct3D 11 pour les développeurs de jeux

Cet article explique comment déployer les composants Direct3D 11 sur un système, si nécessaire.

-   [Vue d’ensemble](#overview)
-   [Direct3D 11,3](#direct3d-113)
-   [Direct3D 11,2](#direct3d-112)
-   [Direct3D 11,1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [Intégration dans les programmes d’installation](#integrating-into-installation-programs)
    -   [Intégration à InstallShield](#integrating-into-installshield)
    -   [Intégration dans un package MSI](#integrating-into-an-msi-package)
-   [Conseils de débogage](#debugging-tips)
-   [Paramètres d’entreprise](#corporate-settings)
-   [Articles connexes](#related-articles)

## <a name="overview"></a>Vue d’ensemble

L’API Direct3D 11 étend l’API Direct3D 10,1 existante avec la prise en charge du rendu multithread et de la création de ressources, du nuanceur de calcul, de la polygonalisation matérielle, de la compression de texture BC6H/BC7 et du modèle de nuanceur HLSL 5,0 avec une liaison de nuanceur dynamique. Outre le composant Direct3D 11, un certain nombre de composants graphiques supplémentaires sont inclus dans le runtime DirectX 11 : Direct3D 11, DXGI 1,1, 10level9 Feature levels, WARP10 Software Rendering Device, Direct2D, DirectWrite et un Direct3D 10,1 mis à jour avec prise en charge de 10level9 et WARP10. Pour plus d’informations sur ces composants graphiques Windows et les autres, consultez [API graphiques dans Windows](graphics-apis-in-windows-vista.md).

Tous ces nouveaux composants graphiques sont intégrés aux systèmes d’exploitation Windows 7 et Windows Server 2008 R2. L’API Direct3D 11 et les composants associés peuvent également être installés sur Windows Vista à l’aide d’une mise à jour du système à partir de Windows Update ; consultez l’article [KB 971644](https://support.microsoft.com/kb/971644)de la base de connaissances. Cette mise à jour nécessite Windows Vista et Service Pack 2. Les utilisateurs finaux avec des mises à jour automatiques activées auront probablement déjà installé les composants Direct3D 11, comme tous les utilisateurs de Windows 7.

L’exemple D3D11InstallHelper est conçu pour simplifier la détection de l’API Direct3D 11, installer automatiquement la mise à jour du système le cas échéant sur l’ordinateur de l’utilisateur final et fournir des messages appropriés à l’utilisateur final lors de la procédure manuelle si un service pack plus récent est requis.

> [!Note]  
> Le compilateur HLSL (D3DCompile \* . dll) et la bibliothèque d’utilitaire D3DX pour Direct3D 11 (D3DX11 \* . dll) ne sont pas intégrés à une version du système d’exploitation Windows, mais ils peuvent être déployés dans le cadre du programme d’installation d’une application à l’aide de la technologie DirectSetup existante. pour plus d’informations sur l’utilisation de DirectSetup, consultez [installation de DirectX pour les développeurs de jeux](/windows/desktop/DxTechArts/directx-setup-for-game-developers) « Effects 11 » est disponible en tant que bibliothèque de prise en charge de source partagée aux [effets de la mise à jour Direct3D 11](https://github.com/Microsoft/FX11). vous pouvez l’inclure directement dans une application (à l’instar de la bibliothèque de l’utilitaire DXUT). Par conséquent, elle n’a pas d’autres exigences de redistribution au moment de l’exécution.

## <a name="direct3d-113"></a>Direct3D 11,3

Windows 10 est fourni avec l’API Direct3D 11,3 intégrée. Consultez [fonctionnalités direct3d 11,3](/windows/desktop/direct3d11/direct3d-11-3-features) pour obtenir la liste des nouvelles fonctionnalités de l’API Direct3D 11,3.

## <a name="direct3d-112"></a>Direct3D 11,2

Windows 8.1 et Windows Server 2012 R2 sont livrés avec l’API Direct3D 11,2 intégrée. Consultez [fonctionnalités direct3d 11,2](/windows/desktop/direct3d11/direct3d-11-2-features) pour obtenir la liste des nouvelles fonctionnalités de l’API Direct3D 11,2.

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 et Windows Server 2012 sont livrés avec l' [API Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) intégrée. La prise en charge partielle de l’API Direct3D 11,1 est disponible sur Windows 7 ou Windows Server 2008 R2 avec la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838) installée. Pour plus d’informations sur la mise à jour de plateforme pour Windows 7, consultez [mise à jour de la plateforme pour Windows 7](platform-update-for-windows-7.md).

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll héberge les fonctionnalités de base pour la détection des composants Direct3D 11 et l’exécution de la mise à jour du système par le biais du service Windows Update, le cas échéant. La DLL n’affiche pas de messages ou de boîtes de dialogue directement.

La DLL se compose des points d’entrée suivants :

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

Cette fonction effectue les vérifications nécessaires et retourne l’état de Direct3D 11 sur cet ordinateur. Cette fonction ne requiert pas de droits d’administrateur.

-   L’État D3D11IH \_ \_ installed indique que Direct3D 11 est déjà installé sur l’ordinateur et qu’il est prêt à être utilisé.
-   \_L’État D3D11IH \_ non \_ pris en charge indique que cette version de Windows ne prend pas en charge Direct3D 11 ou les technologies associées.
-   L’État D3D11IH \_ état \_ requis \_ dernier \_ SP indique que la dernière version de Windows Vista service pack doit être installée par l’utilisateur.
-   Enfin, l’État D3D11IH \_ Status \_ require \_ Update indique que Direct3D 11 n’est pas installé sur le système, mais que la mise à jour du système s’applique à cette version de Windows.

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

Cette fonction utilise l’API Windows Update pour effectuer la mise à jour du système pour l’installation de Direct3D 11 sur ce système, le cas échéant. Notez que cette fonction nécessite une connexion réseau pour Windows Update, ainsi que des droits d’administration. Elle prend une fonction de rappel de progression facultative et un pointeur de contexte utilisateur, et retourne un code de résultat final une fois terminé.

-   Le résultat de la \_ \_ réussite de D3D11IH indique que la mise à jour du système a été appliquée et est prête à être utilisée, tandis que le redémarrage de la réussite de D3D11IH \_ \_ \_ indique que la mise à jour du système nécessite un redémarrage de l’ordinateur avant la fin de son exécution. Notez que cette fonction ne planifie pas un redémarrage du système.
-   \_Le résultat D3D11IH \_ non \_ pris en charge indique que la mise à jour du système ne s’applique pas à cette version de Windows. Ce résultat ne doit pas se produire si cette fonction est appelée uniquement après l’obtention d’un \_ État D3D11IH \_ nécessite l' \_ État de mise à jour de CheckDirect3D11Status.
-   Le résultat de la \_ \_ mise à jour du résultat D3D11IH \_ \_ introuvable indique que le package de mise à jour système est introuvable sur les serveurs Windows Update.
-   En cas d’échec du téléchargement de Windows Update ou de l’installation, le téléchargement de la \_ \_ mise à jour du résultat D3D11IH \_ \_ a échoué ou \_ \_ l’installation de la mise à jour du résultat D3D11IH \_ \_ est retournée comme résultat.
-   Si une erreur de connectivité réseau est retournée à partir de l’API Windows Update, le résultat de l' \_ erreur de service Wu de résultat D3D11IH \_ \_ \_ est retourné, indiquant que le problème peut être intermittent ou lié à la configuration réseau ou aux paramètres de pare-feu. Toute tentative de mise à jour de la fonction peut être effectuée.

</dd> </dl>

Pour plus d’informations sur l’API Windows Update, consultez [Windows Update API de l’agent](/windows/desktop/Wua_Sdk/portal-client).

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe nécessite l’exécution de D3D11InstallHelper.dll.

D3D11Install.exe est un outil qui permet d’utiliser des D3D11InstallHelper.dll en tant que programme d’installation autonome avec l’interface utilisateur et les messages de l’utilisateur final, ainsi que d’agir comme exemple pour une utilisation correcte de la DLL. Le processus se termine avec 0 si Direct3D 11 est déjà installé, si la mise à jour du système s’applique correctement sans nécessiter un redémarrage du système, si une installation de Service Pack est requise ou si Direct3D 11 n’est pas pris en charge par cet ordinateur. La valeur 1 est retournée si la mise à jour du système est correctement appliquée et nécessite un redémarrage du système. Un 2 est retourné pour d’autres conditions d’erreur. Notez que ce fichier exécutable nécessite des droits d’administrateur pour s’exécuter et qu’il possède un manifeste qui demande une élévation lorsqu’il est exécuté sur Windows Vista ou Windows 7 avec le contrôle de compte d’utilisateur activé. D3D11Install.exe peut être utilisé en tant qu’outil autonome pour déployer la mise à jour Direct3D 11, ou elle peut être utilisée directement par des programmes d’installation.

Il prend en charge les commutateurs de ligne de commande suivants :

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/quiet 
</dt> <dd>

N’affiche aucun message, invites, boîtes de dialogue de progression ou messages d’erreur.

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/passive 
</dt> <dd>

N’affiche aucun message, invite ou message d’erreur, mais affiche la boîte de dialogue État d’avancement.

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

Affiche uniquement les invites minimales.

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

Supprime les invites de confirmation de l’installation de la mise à jour, si nécessaire et applicable, pour une installation standard et minimale.

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid décimal 
</dt> <dd>

Force le code d’identificateur de langue à utiliser lors de l’affichage des messages de l’utilisateur final et des ressources de boîte de dialogue. La valeur par défaut est 1024, qui utilise le paramètre de langue par défaut du système.

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

Force l’utilisation de Windows Update plutôt que la valeur système par défaut, qui peut être Windows Server Update Services (WSUS) s’exécutant sur un serveur géré ou une autre configuration non standard.

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>Intégration dans les programmes d’installation

Pour se conformer à la facilité d’installation, à l' [exigence technique 3,1 pour les jeux pour Windows](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006), vous devez veiller à ce que les invites des utilisateurs finaux soient présentées au début du processus d’installation et pour s’assurer qu’il n’y a pas plusieurs invites d’élévation associées au contrôle de compte d’utilisateur. Il existe trois choix de base pour atteindre cet objectif :

1.  La méthode la plus simple consiste à exécuter le D3D11Install.exe avec le commutateur de ligne de commande **/minimal**. Cela doit être fait tôt dans le programme d’installation Q&A, et l’installation doit utiliser la valeur de retour 1 pour indiquer qu’un redémarrage doit être planifié à la fin de l’installation. L’exécution du programme requiert des droits d’administration.
2.  Utilisez D3D11InstallHelper.dll directement pour détecter la nécessité de la mise à jour, en fournissant tous les messages de l’utilisateur final nécessaires à l’État D3D11IH \_ état \_ nécessite le \_ dernier \_ SP, où la résolution requiert des opérations manuelles de l’utilisateur. Le résultat de l’état \_ D3D11IH \_ non \_ pris en charge peut être utilisé pour contrôler l’installation des ressources associées à Direct3D 11, ou en tant que condition d’erreur pour les applications Direct3D 11 uniquement, mais il ne s’agit pas nécessairement d’un message utilisateur final utile. Pour l’État D3D11IH l’état \_ \_ requiert \_ Update, le programme d’installation peut utiliser directement le point d’entrée de la dll DoUpdateForDirect3D11 pour effectuer la mise à jour et gérer les divers messages utilisateur finaux résultants. Vous pouvez trouver des exemples de messages standard en consultant la boîte de dialogue D3D11Install.exe et les ressources de table de chaînes. Le point d’entrée de mise à jour requiert des droits d’administrateur.
3.  Une approche hybride consiste à vérifier l’état avec D3D11InstallHelper.dll et, dans le cas du code d’État D3D11IH, le \_ \_ \_ dernier \_ État du SP ou D3D11IH \_ \_ doit \_ être Update, D3D11Install.exe peut être exécuté avec les commutateurs **/minimal** et **/y** pour afficher la boîte de dialogue ou pour effectuer la mise à jour, si nécessaire. Ces étapes doivent être effectuées au début du processus d’installation, généralement immédiatement après le Q&A, et l’exécution de l’exécutable nécessite des droits d’administration.

### <a name="integrating-into-installshield"></a>Intégration à InstallShield

La gestion du déploiement de Direct3D 11 à partir de l’InstallScript d’InstallShield s’effectue facilement à l’aide de l’exemple D3D11InstallHelper. Les étapes requises pour l’intégration à InstallShield à l’aide d’InstallScript sont les suivantes (à l’aide de la méthode 3, décrite dans la section précédente) :

1.  Ouvrez un projet InstallScript dans l’éditeur InstallShield.
2.  Ajoutez D3D11InstallHelper.dll et D3D11Install.exe au projet dans les **fichiers de support**.

    **Pour ajouter les fichiers au projet InstallShield**

    1.  Sous l’onglet **Concepteur d’installation** , cliquez sur fichiers de **support/panneaux** d’exploration sous **comportement et logique** dans le volet de navigation à gauche.
    2.  Cliquez sur indépendant de la **langue**, puis cliquez avec le bouton droit dans la fenêtre **fichiers** et sélectionnez **Insérer des fichiers**. Accédez à ajouter D3D11InstallHelper.dll et D3D11Install.exe. L’emplacement par défaut de ces fichiers est : exemples racine SDK \\ \\ C++ \\ misc \\ bin \\ x86

3.  Dans l’Explorateur InstallScript, cliquez sur le fichier InstallScript (généralement Setup. vie utile restante) qui appellera la DLL ou le fichier exécutable, situé sous **comportement et logique** dans le volet de navigation de gauche.
4.  Collez l’InstallScript suivant dans le fichier vers le haut :

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  Collez l’InstallScript suivant dans le fichier dans la fonction **OnFirstUIBefore** , juste avant le retour 0 :

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a>Intégration dans un package MSI

Vous trouverez ci-dessous une description détaillée des étapes requises pour intégrer le déploiement de Direct3D 11 à l’aide d’actions personnalisées MSI (à l’aide de la méthode 3, décrite précédemment dans cette rubrique) :

1.  Ajoutez une propriété à la table de propriétés MSI appelée **RelativePathToD3D11IH** qui contient le chemin d’accès relatif à D3D11Install.exe et D3D11InstallHelper.dll lors de l’installation (généralement dans l’image de média). Cela définit également une propriété MSI D3D11IH \_ Status sur l’état renvoyé par CheckDirect3D11Status (une propriété de type chaîne égale au symbole d’énumération ou « Error »).
2.  Après l’action CostFinalize, appelez la fonction D3D11InstallHelper.dll **SetD3D11InstallMSIProperties** en tant qu’action personnalisée immédiate pour définir les propriétés MSI appropriées pour les autres actions personnalisées.
3.  Lors de l’installation, déclenchez une action personnalisée différée après l’action InstallFiles qui appelle la fonction D3D11InstallHelper.dll **DoD3D11InstallUsingMSI**. L’action personnalisée doit définir l’indicateur msidbCustomActionTypeNoImpersonate pour qu’elle s’exécute dans un contexte avec élévation de privilèges.
4.  Après l’action InstallFinalize, appelez la fonction D3D11InstallHelper.dll **FinishD3D11InstallUsingMSI** en tant qu’action personnalisée immédiate pour gérer le code de résultat de la demande de redémarrage réussi, si nécessaire.

Cette procédure est décrite en détail dans les instructions suivantes, qui décrivent un processus qui peut être effectué à l’aide d’un éditeur MSI, tel que l' [éditeur Orca](/windows/desktop/Msi/orca-exe). Certains éditeurs MSI possèdent des assistants qui simplifient certaines de ces étapes de configuration.

**Pour configurer un package MSI en vue de l’intégrer à D3D11InstallHelper.dll**

1.  Ouvrez le package MSI dans Orca.
2.  Ajoutez la ligne indiquée dans le tableau suivant à la table binaire dans le package MSI.

    | Nom    | Données                                         |
    |---------|----------------------------------------------|
    | D3D11IH | Chemin d’accès au fichier DLL \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Ce fichier sera incorporé dans le package MSI. vous devez donc effectuer cette étape chaque fois que vous recompilez D3D11InstallHelper.dll.

     

3.  Ajoutez les lignes indiquées dans le tableau suivant à la table CustomAction dans le package MSI. 

    | Action              | Type                                                                                                                                                                   | Source  | Cible                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137 | D3D11IH | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | FinishD3D11InstallUsingMSI   |

    

     

4.  Ajoutez les valeurs indiquées pour action, condition et séquence dans le tableau suivant à la table InstallExecuteSequence dans le package MSI. 

    | Action              | Condition     | Séquence | Notes                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | Le numéro de séquence place l’action juste après CostFinalize.                                                                                                 |
    | Direct3D11DoInstall | NON installé | 4004     | Cette action personnalisée se produit uniquement au cours d’une nouvelle installation pour tous les utilisateurs. Le numéro de séquence place l’action après InstallFiles et après les restaurations. |
    | Direct3D11Finish    |               | 6615     | Le numéro de séquence place l’action juste après InstallFinalize.                                                                                              |

    

     

5.  Ajoutez la ligne indiquée dans le tableau suivant à la table des **Propriétés** dans le package MSI. 

    | Propriété              | Valeur                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11IH | chemin de fichier relatif qui contient D3D11Install.exe et D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > L’emplacement spécifié par le chemin d’accès est relatif à l’emplacement spécifié par le chemin d’installation, par exemple, « Redist \\ ».

     

6.  Enregistrez le package MSI. Pour plus d’informations sur les packages et les Windows Installer MSI, consultez [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Conseils de débogage

D3D11InstallHelper.dll et D3D11Install.exe peuvent être générés avec la configuration Debug dans Visual Studio, et ces versions impriment les messages dans le mécanisme de sortie de débogage Windows standard.

## <a name="corporate-settings"></a>Paramètres Entreprise

L’exemple D3D11InstallHelper est conçu pour un déploiement standard via Windows Update, qui est le scénario le plus courant pour l’installation d’un jeu par les consommateurs. Toutefois, de nombreux développeurs de jeux, travaillant pour les éditeurs et les Studios de développement, le font dans les paramètres d’entreprise qui disposent d’un serveur géré localement fournissant des mises à jour logicielles à l’aide de la technologie Windows Server Update Services (WSUS). Dans ce type d’environnement, l’administrateur informatique local a le contrôle de l’approbation des mises à jour qui sont mises à disposition des ordinateurs au sein du réseau d’entreprise, et la version standard du client de la mise à jour KB 971644 n’est pas disponible.

Il existe trois solutions de base pour le déploiement de DirectX 11 dans les paramètres d’entreprise/entreprise :

-   Dans certaines configurations, il est possible de vérifier directement Windows Update plutôt que d’utiliser le serveur WSUS géré localement. Pour cette raison, D3D11InstallHelper prend en charge le commutateur de ligne de commande **/Wu** . Toutefois, tous les réseaux d’entreprise n’autorisent pas les connexions aux serveurs publics Microsoft.
-   L’administrateur informatique local peut approuver KB 971512, une mise à jour prise en charge par l’entreprise, déployée à partir de WSUS, qui comprend l’API Direct3D 11. Il s’agit de la seule option permettant à un utilisateur standard d’obtenir la mise à jour de Direct3D 11 dans un environnement entièrement verrouillé.
-   Vous pouvez également installer manuellement [KB 971512](https://support.microsoft.com/kb/971512/) .

Il est très rare que l’ordinateur d’un joueur puisse uniquement obtenir des mises à jour à partir d’un serveur WSUS géré localement, et il ne s’agit que de développeurs appartenant à des organisations de grande taille qui sont susceptibles d’être dans de tels environnements.

## <a name="related-articles"></a>Articles connexes

[Pare-feu Windows pour les développeurs de jeux](/windows/desktop/DxTechArts/games-and-firewalls)

[Explorateur de jeux Windows pour les développeurs de jeux](/windows/desktop/DxTechArts/windows-game-explorer-integration)