---
description: Msizap.exe est un utilitaire de ligne de commande qui supprime toutes les informations Windows Installer d’un produit ou de tous les produits installés sur un ordinateur. Les produits installés par le programme d’installation peuvent ne pas fonctionner après l’utilisation de Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011841"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe est un utilitaire de ligne de commande qui supprime toutes les informations Windows Installer d’un produit ou de tous les produits installés sur un ordinateur. Les produits installés par le programme d’installation peuvent ne pas fonctionner après l’utilisation de Msizap.

sur Windows 2000 et Windows XP, des privilèges d’administrateur sont nécessaires pour utiliser Msizap.exe.

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md) et ne doit pas être redistribué. utilisez la version récente de Msizap.exe (version 3.1.4000.2726 ou ultérieure) qui est disponible dans les composants SDK Windows pour les développeurs Windows Installer pour Windows Vista ou version ultérieure. Les versions plus petites de Msizap.exe peuvent supprimer des informations sur toutes les mises à jour qui ont été appliquées à d’autres applications sur l’ordinateur de l’utilisateur. Si ces informations sont supprimées, ces autres applications devront peut-être être supprimées et réinstallées pour recevoir des mises à jour supplémentaires.

## <a name="syntax"></a>Syntaxe

**Msizap T**_\[ wa ! \] {code produit}_

**Msizap T**_\[ wa ! \] <msi package>_

**\* *** Msizap \[ WA ! \]* **ALLPRODUCTS**

**Msizap PWSA ?!**

## <a name="command-line-options"></a>Options de la ligne de commande

Msizap.exe utilise les options de ligne de commande qui ne respectent pas la casse présentées dans le tableau suivant.



| Option | Description                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | supprime tous les dossiers et clés de registre Windows Installer, ajuste les nombres de DLL partagées et arrête Windows Installer service. Supprime également les informations de clé In-Progress et de restauration.                                                                           |
| a      | Modifie uniquement les ACL pour le contrôle total de l’administrateur pour une suppression spécifiée.                                                                                                                                                                                            |
| g      | pour tous les utilisateurs, supprime tous les fichiers de données Windows Installers mis en cache qui ont été orphelins.                                                                                                                                                                       |
| p      | Supprime la clé de In-Progress.                                                                                                                                                                                                                                  |
| s      | Supprime les informations de restauration.                                                                                                                                                                                                                                 |
| t      | Supprime toutes les informations pour le code de produit spécifié. Lorsque vous utilisez cette option, mettez le code du produit entre accolades. Cette option peut être utilisée avec le chemin d’accès complet au fichier .msi ou avec le code du produit.                                        |
| w      | supprime Windows Installer informations pour tous les utilisateurs. Lorsque cette option n’est pas définie, seules les informations de l’utilisateur actuel sont supprimées. L’utilisation de cette option nécessite le chargement du profil de l’utilisateur afin que la ruche du Registre par utilisateur soit disponible. |
| ?      | Aide détaillée.                                                                                                                                                                                                                                                 |
| !      | Force une réponse « oui » à une invite.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



