---
description: La définition de la valeur de cette stratégie système par ordinateur sur &\# 0034 ; 1&\# 0034 ;, permet aux utilisateurs non administratifs d’installer des applications gérées à partir de sources stockées sur des supports, comme un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869605"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

La définition de la valeur de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » permet aux utilisateurs non administratifs d’installer des [*applications gérées*](m-gly.md) à partir de sources stockées sur un support, par exemple un CD-ROM. Consultez [résilience source](source-resiliency.md). Par exemple, si cette stratégie est définie, un utilisateur non administratif peut utiliser une source de média pour installer des applications ou des applications attribuées ou publiées en cours d’installation pour tous les utilisateurs. La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes sur des privilèges LocalSystem au cours d’une installation avec élévation de privilèges.

La valeur par défaut de cette stratégie est 1 uniquement sur les ordinateurs exécutant Windows Vista et qui ne sont pas joints à un domaine. Par défaut sur les autres ordinateurs, les utilisateurs non-administrateurs ne peuvent pas installer des applications gérées à partir d’une source située sur un support.

Étant donné que cette stratégie permet aux utilisateurs qui ne sont pas administrateurs d’installer avec des privilèges qu’ils n’ont pas par défaut, avant de définir cette stratégie, vous devez déterminer si elle fournit un niveau de sécurité approprié à votre utilisateur. Le paramètre par défaut est recommandé pour garantir un environnement sécurisé.

Pour plus d’informations sur la sécurisation des installations et l’utilisation des certificats numériques, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md) et [téléchargement d’une installation à partir d’Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Notes

La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes arbitraires sur des privilèges LocalSystem s’ils disposent d’un package Windows Installer qui installe ou lance ces programmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



