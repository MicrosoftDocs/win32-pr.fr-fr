---
description: En plus d’être accessibles par le biais de l’interface IVssBackupComponents au moyen de l’objet Device de sa copie, un demandeur peut rendre disponible un cliché instantané pour d’autres processus en tant qu’appareil en lecture seule monté.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Exposition et revêtement des volumes clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413374"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Exposition et revêtement des volumes clichés instantanés

En plus d’être accessibles par le biais de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) au moyen de l' [*objet Device*](vssgloss-d.md)de sa copie, un demandeur peut rendre disponible un cliché instantané pour d’autres processus en tant qu’appareil en lecture seule monté.

Ce processus est connu sous le nom [*d’exposition d’un cliché instantané*](vssgloss-e.md)et est effectué à l’aide de la méthode [**IVssBackupComponents :: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .

Un cliché instantané peut être exposé en tant que volume local (une lettre de lecteur ou associée à un dossier monté) ou un partage de fichiers.

Pour illustrer ce cas, envisagez d’utiliser un cliché instantané d’un volume sur le système exposedSys monté sur F : \\ sur dont la racine est les répertoires dirOne et dirTwo, et le fichier FileOne.

## <a name="exposing-a-shadow-copy-locally"></a>Exposition locale d’un cliché instantané

Lorsqu’il est monté en tant que volume local, la racine du cliché instantané est toujours visible au niveau du point de montage (lettre de lecteur ou dossier monté) et tous les fichiers copiés par des clichés instantanés sont visibles.

Si le cliché instantané a été exposé localement par le biais du dossier monté C : \\ ShadowOfF, vous trouverez tous les fichiers présents sur le disque monté à F : \\ au moment du cliché instantané disponible sous C : \\ ShadowOfF. L’examen de C : \\ ShadowOfF révèle deux répertoires, dirOne et dirTwo, et un fichier, fileOne, sous C : \\ ShadowOfF.

Un appel à exposer localement le cliché instantané peut être :

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

Si le cliché instantané a été correctement exposé localement, *wszExposed* doit contenir la chaîne de caractères larges « C : \\ ShadowOfF ».

Le cliché instantané peut être non exposé ultérieurement en appelant [**IVssBackupComponentsEx2 :: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).

Seuls les clichés instantanés persistants, à savoir, les clichés instantanés créés à l’aide de VSS \_ CTX \_ NAS \_ Rollback ou VSS \_ \_ application \_ Rollback, peuvent être exposés localement.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Exposition d’un cliché instantané en tant que partage distant

Vous pouvez également choisir de rendre le cliché instantané du disque monté sur F : \\ disponible en tant que partage de fichiers distant et d’exposer uniquement les données sous dirTwo en tant que partage de fichiers dirTwoOfF.

Dans ce cas, les systèmes peuvent accéder au cliché instantané des fichiers sous F : \\ dirTwo en mappant \\ \\ exposedSys \\ dirTwoOfF en tant que lecteur réseau.

Un appel permettant d’implémenter à distance d’exposer le cliché instantané en tant que partage peut être le suivant :

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

Si le cliché instantané a été exposé à distance avec succès, *wszExposed* doit contenir la chaîne de caractères larges « dirTwoOfF ».

Tout système qui mappe actuellement le partage réseau de dirTwoOfF peut se déconnecter de celui-ci, tout comme il peut se déconnecter de n’importe quel partage ordinaire.

## <a name="surfacing-a-shadow-copy"></a>Revêtement d’un cliché instantané

Un cliché [*instantané superficiel*](vssgloss-s.md) est un cliché instantané dans lequel le cliché instantané est connu pour l’espace de noms du gestionnaire de montage d’un système.

Cela signifie que vous pouvez localiser ces clichés instantanés comme vous le feriez pour tout autre volume disponible mais pas encore monté, en utilisant **FindFirstVolume** et **FindNextVolume**, par exemple.

En clair, les clichés instantanés exposés sont également des clichés instantanés en surface. Toutefois, l’inverse n’est pas nécessairement vrai.

Si un cliché instantané exposé localement a été démonté, ou si un système a choisi de déconnecter un cliché instantané exposé à distance, ce cliché instantané n’est plus exposé. Toutefois, tant que le cliché instantané est rendu persistant, les volumes sont exposés. Cela signifie qu’elles peuvent être montées comme tout autre volume en lecture seule.

 

 



