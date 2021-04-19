---
description: Donne une vue d’ensemble des modifications apportées aux contrôles parentaux Windows introduits dans Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Nouveautés dans les contrôles parentaux Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530087"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Nouveautés des contrôles parentaux Windows 7

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Vue d’ensemble des modifications du contrôle parental pour Windows 7

L’objectif de ce document est de fournir une vue d’ensemble des modifications apportées aux contrôles parentaux Windows introduits dans Windows 7 et de permettre aux fournisseurs de solutions de contrôle parental tiers de tirer parti de ces modifications. Ce document part du principe que les lecteurs sont familiers avec les contrôles de contrôle parental pour Windows Vista et qu’ils reflètent uniquement les modifications apportées à cette fonctionnalité dans Windows 7 qui sont pertinentes pour le développement de solutions de contrôle parental tierces. Une mise à jour complète de la documentation sur le contrôle parental de Windows MSDN sera suivie à une date ultérieure.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Décisions de conception clés pour les modifications du contrôle parental Windows 7

Les modifications apportées aux contrôles parentaux introduits dans Windows 7 poursuivent l’objectif principal de la promotion de la coexistence de solutions de contrôle parental tierces avec la fonctionnalité intégrée. Les modifications sont les suivantes :

-   Suppression du filtrage Web et des rapports d’activité à partir de la fonctionnalité de contrôle parental intégrée. Les contrôles de contrôle parental fournis fournissent des restrictions principales mises en œuvre par Microsoft, telles que les limites de temps, les restrictions d’application et les restrictions de jeux. Le filtrage Web, les rapports d’activité et d’autres fonctionnalités peuvent être fournis par Microsoft ou des solutions de contrôle parental tierces. Par exemple, la solution de sécurité de la famille Windows Live permet le filtrage Web, la gestion à distance et la surveillance des activités, ainsi que la gestion des contacts pour toutes les applications Windows Live.
-   L’activation de solutions tierces pour remplacer l’interface utilisateur de configuration du fournisseur intégré tout en continuant à utiliser l’implémentation intégrée des restrictions de temps, d’application et de jeu.
-   Activation de la découverte et de l’activation de solutions tierces sur l’ordinateur par un parent ou un gardien (compte administrateur).

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Modifications de l’interface utilisateur de niveau supérieur des contrôles parentaux dans Windows 7

Windows 7 apporte les modifications suivantes à l’interface utilisateur du panneau de configuration du contrôle parental :

-   La section contrôles supplémentaires est présentée, dans laquelle vous pouvez sélectionner des contrôles qui fournissent des fonctionnalités supplémentaires, telles que le filtrage Web, les rapports d’activité, etc., dans une zone de liste déroulante. Microsoft ou des fournisseurs tiers doivent inscrire leurs solutions avec les contrôles parentaux Windows 7 pour pouvoir les sélectionner dans la zone de liste déroulante contrôles supplémentaires. Pour plus d’informations sur l’inscription d’une solution, consultez inscription du fournisseur, plus loin dans cette rubrique).
-   L’image du logo du fournisseur actuellement sélectionné s’affiche dans l’angle supérieur droit de la page.
-   Les vignettes de l’utilisateur géré peuvent afficher un résumé des paramètres de contrôle parental fournis par le fournisseur actuellement sélectionné.

Le fournisseur actuellement sélectionné peut choisir d’utiliser sa propre interface utilisateur pour les écrans de contrôle utilisateur pour les utilisateurs gérés, ou il peut choisir de s’appuyer sur l’implémentation WPC de cet écran. L’implémentation intégrée présente les modifications suivantes apportées à ses éléments :

-   La section rapport d’activité est supprimée.
-   Le lien permettant d’afficher les rapports d’activité est supprimé.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Vue d’ensemble de l’API de contrôle parental : modifications apportées à Windows 7

Le mécanisme d’intégration pour les fournisseurs de solutions tiers a été étendu pour permettre :

-   Inscription du fournisseur. Lors de l’inscription, un fournisseur devient sélectionnable dans la zone de liste déroulante contrôles supplémentaires de l’écran du panneau de configuration contrôle parental.
-   Interrogation du fournisseur actuellement sélectionné. Une interface COM publique est exposée pour activer cette fonctionnalité.
-   New est également l’ensemble des interfaces COM qui doivent être implémentées par les fournisseurs pour autoriser :
    -   Activation ou désactivation du fournisseur par WPC lors de la sélection par l’utilisateur de contrôles supplémentaires.
    -   WPC pour transmettre le contrôle au fournisseur afin de configurer les paramètres de contrôle parental de l’utilisateur géré.
    -   WPC pour interroger le fournisseur sur le résumé des paramètres de contrôle parental de l’utilisateur géré.

## <a name="third-party-provider-integration"></a>Intégration d’un fournisseur tiers

### <a name="provider-registration"></a>Inscription du fournisseur

Pour inscrire un nouveau fournisseur avec contrôle parental, une valeur de registre doit être écrite dans la clé fournisseurs des contrôles parentaux Windows. Le nom de la valeur est un GUID unique utilisé pour identifier le fournisseur. La valeur Data est le chemin d’accès à une clé de Registre dans **HKEY \_ local \_ machine** qui contient des informations sur le fournisseur.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Parental Controls
                  Providers
                     {45D63315-0824-4df4-B8A4-EF137D8810D1} = SOFTWARE\Microsoft\Family Safety\WPC\
```

À l’emplacement de la clé de Registre spécifié, les valeurs suivantes sont attendues.



| Terme                                                                                                                 | Description                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Chemin d’accès complet à un fichier binaire de ressource avec un ID de ressource négatif pour l’image du logo du fournisseur (stocké en tant que **\_ bitmap d’image**).<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**<br/> | Chemin d’accès qualifié complet à un fichier binaire de ressource avec un ID de ressource négatif pour le nom du fournisseur. La longueur **DisplayName** ne doit pas dépasser 50 caractères.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**<br/> | Chemin d’accès qualifié complet à un fichier binaire de ressource avec un ID de ressource négatif pour la description du fournisseur. La longueur de la description ne doit pas dépasser 200 caractères.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | ID de classe de la classe du fournisseur qui implémente IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | ID de classe de la classe du fournisseur qui implémente IWPCProviderConfig. **StateCLSID** et **ConfigCLSID** peuvent être identiques.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Valeur différente de zéro **DWORD** facultative qui spécifie que le contrôle parental Windows affiche un lien vers l’écran système de classification du jeu après qu’un fournisseur est sélectionné comme nouveau fournisseur actuel.<br/> |



 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Family Safety
            WPC
               LogoImage = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40001
               DisplayName = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40002
               Description = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40003
               StateCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               ConfigCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               GRSVisible = 0x00000001 (1)
```

Le panneau de configuration du contrôle parental utilise **LogoImage**, **DisplayName** et **Description** pour modifier la page principale du panneau de configuration du contrôle parental lorsque ce fournisseur est sélectionné. La valeur **StateCLSID** est utilisée lorsque le fournisseur est activé ou désactivé. La valeur **ConfigCLSID** est utilisée lorsque l’interface utilisateur obtient des informations dynamiques sur chaque utilisateur (c’est le cas uniquement si le fournisseur est actuellement sélectionné).

 

 




