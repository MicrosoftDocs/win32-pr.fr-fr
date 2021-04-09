---
description: La mise à jour corrective du contrôle de compte d’utilisateur permet aux auteurs d’installations Windows Installer d’identifier les correctifs signés numériquement qui peuvent être appliqués ultérieurement par des utilisateurs non-administrateurs.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Mise à jour corrective du contrôle de compte d’utilisateur (UAC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868833"
---
# <a name="user-account-control-uac-patching"></a>Mise à jour corrective du contrôle de compte d’utilisateur (UAC)

La mise à jour corrective du [*contrôle de compte d’utilisateur*](u-gly.md) permet aux auteurs d’installations Windows Installer d’identifier les correctifs signés numériquement qui peuvent être appliqués ultérieurement par des utilisateurs non-administrateurs.

Si la signature numérique ne correspond pas au certificat, Windows Vista affiche une boîte de dialogue UAC demandant l’autorisation de l’administrateur avant d’installer le correctif. Sur les systèmes antérieurs à Windows Vista, le programme d’installation n’applique pas un correctif signé qui ne correspond pas au certificat.

Si un non-administrateur tente d’appliquer un correctif à une application et que les conditions suivantes ne sont pas remplies, Windows Vista notifie l’utilisateur que l’autorisation de l’administrateur est requise avant d’installer le correctif. Un non-administrateur peut poursuivre l’installation du correctif, sans qu’il soit nécessaire d’obtenir des autorisations d’administrateur supplémentaires, à condition que les conditions suivantes soient remplies.

-   L’application a été installée sur Windows Vista ou Windows XP à l’aide de Windows Installer 3,0 ou version ultérieure.

    **Windows Server 2008 :** Non pris en charge.

-   Si l’application a été installée sur Windows XP, l’application doit également avoir été installée à partir d’un support amovible, tel qu’un CD-ROM ou un DVD. Cette restriction ne s’applique pas si l’application a été installée sur Windows Vista.
-   L’application n’a pas été installée à partir d’une image source [d’installation administrative](administrative-installation.md) .
-   L’application a été installée à l’origine par ordinateur. Pour plus d’informations sur la façon de permettre aux non-administrateurs d’appliquer des correctifs logiciels à des applications gérées par l’utilisateur une fois que le correctif a été approuvé par un administrateur, consultez Mise à [jour corrective Per-User applications gérées](patching-per-user-managed-applications.md).
-   La [table MsiPatchCertificate](msipatchcertificate-table.md) est présente dans le package du programme d’installation de Windows (fichier. msi) et contient les informations nécessaires pour activer le contrôle de compte d’utilisateur. La table et les informations ont peut-être été incluses dans le package d’installation d’origine ou ajoutées au package par un fichier correctif Windows Installer (fichier. msp).
-   Les correctifs sont signés numériquement par un certificat répertorié dans le [tableau MsiPatchCertificate](msipatchcertificate-table.md). Pour plus d’informations sur les certificats de signature numérique, consultez [signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).
-   La signature numérique sur le package de correctifs peut être vérifiée par rapport au certificat figurant dans la [table MsiPatchCertificate](msipatchcertificate-table.md). Pour plus d’informations sur l’utilisation de signatures numériques, de certificats numériques et de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), consultez la section [sécurité](https://msdn.microsoft.com/library/cc527452.aspx) du kit de développement logiciel (SDK) Microsoft Windows.
-   Le certificat de signataire utilisé pour vérifier la signature numérique sur le package de correctifs est valide et n’a pas été révoqué.
    > [!Note]  
    > Bien que vous ne pouvez pas signer un correctif à l’aide d’un certificat expiré, l’évaluation d’une signature numérique sur un correctif n’échoue pas si le certificat a expiré. L’évaluation utilise la [table MsiPatchCertificate](msipatchcertificate-table.md)en cours, qui se compose de la table MsiPatchCertificate dans le package d’origine et de toute modification apportée à la table par les correctifs séquencés avant celle en cours. Un correctif peut ajouter de nouveaux certificats à la table MsiPatchCertificate pour évaluer les correctifs séquencés après le correctif actuel. Un certificat révoqué est toujours rejeté.

     

-   La mise à jour corrective des privilèges minimaux n’a pas été désactivée en définissant la propriété [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) ou la stratégie [DisableLUAPatching](disableluapatching.md) .

Un correctif appliqué à l’aide de la mise à jour corrective UAC peut également être supprimé par un non-administrateur.

Les administrateurs peuvent appliquer des correctifs aux produits installés par ordinateur, quel que soit le paramètre de contrôle de compte d’utilisateur de l’application.

Vous pouvez déterminer si la mise à jour corrective des privilèges minimum est activée pour une application à l’aide de la fonction [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) pour interroger la propriété de l' \_ \_ application Lua autorisée INSTALLPROPERTY \_ , ou en utilisant la méthode [**ProductInfo**](installer-productinfo.md) pour interroger la propriété « AuthorizedLUAApp ». Si la valeur de l’une des propriétés est 1, l’application est activée pour la mise à jour corrective des comptes d’utilisateur de moindre privilège.

Un administrateur peut désactiver la mise à jour corrective des privilèges minimaux sur l’ordinateur en affectant la valeur 1 à la stratégie [DisableLUAPatching](disableluapatching.md) . Vous pouvez affecter la valeur 1 à la propriété [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) lors de l’installation initiale d’une application afin d’empêcher la mise à jour corrective de moindre privilège pour cette application uniquement.

Cette fonctionnalité est disponible à partir de Windows Installer version 3,0. La mise à jour corrective du contrôle de compte d’utilisateur (UAC) a été appelée mise à jour corrective du compte d’utilisateur avec privilèges minimum dans Windows XP. La mise à jour corrective LUA n’est pas disponible sur Windows 2000 et Windows Server 2003.

Pour plus d’informations sur la compatibilité des applications et le développement d’applications compatibles avec le contrôle de compte d’utilisateur (UAC), consultez les informations UAC fournies sur [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

 

 
