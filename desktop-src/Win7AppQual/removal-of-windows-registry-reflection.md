---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Suppression de la réflexion du Registre Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522191"
---
# <a name="removal-of-windows-registry-reflection"></a>Suppression de la réflexion du Registre Windows

## <a name="platform"></a>Plateforme

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

Le processus de réflexion du Registre copie les clés de Registre et les valeurs entre deux vues du Registre pour les maintenir synchronisées. Dans les précédentes installations 64 bits de Windows, le processus reflétait un sous-ensemble des clés de Registre redirigées entre les vues 32 bits et 64 bits. Toutefois, l’implémentation de cela provoquait des incohérences dans l’état du Registre. (Pour plus d’informations sur la réflexion du Registre, consultez l’article MSDN correspondant dans la section *liens vers d’autres ressources* ci-dessous.)

À compter de Windows 7, nous avons supprimé complètement la réflexion du Registre et fusionné les clés qui ont utilisé pour être reflétées :

-   HKEY \_ local \_ machine \\ classes de logiciels \\
-   HKEY \_ local \_ machine \\ Software \\ Microsoft \\ COM3
-   HKEY \_ local \_ machine \\ Software \\ Microsoft \\ EventSystem
-   HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE
-   HKEY \_ local \_ machine \\ Software \\ Microsoft \\ RPC
-   \_Classes de \\ \* \\ logiciels \\ de HKEY Users
-   \_Classes HKEY Users \\ \* \_

En fait, cela fournit le même comportement de réflexion, car les modifications apportées immédiatement à ces clés sont disponibles pour les applications 32 bits et 64 bits.

Les clés qui ont été représentées de manière conditionnelle restent fractionnées :

-   HKEY \_ local \_ machine \\ classes de logiciels \\ \\ CLSID
-   HKEY \_ local \_ machine \\ classes logicielles ( \\ \\ interface)
-   \_CLSID des \\ \* \\ classes de logiciels \\ \\ de l’utilisateur
-   HKEY \_ Users, \\ \* \\ classes de logiciels ( \\ \\ interface)
-   \_CLSID des \\ \* \_ classes \\ de l’utilisateur HKEY
-   \_ \\ \* \_ Interface classes de HKEY Users \\

Ils sont utilisés pour conserver les données qui ne doivent pas être partagées entre les applications 32 bits et 64 bits.

## <a name="manifestation"></a>Manifestation

Les clés CLSID et interface de la liste ci-dessus ne sont plus reflétées alors qu’elles sont toujours redirigées. Bien qu’il s’agit du comportement souhaité dans la plupart des cas, il est possible que les applications prennent une dépendance sur leur comportement réfléchi dans Vista.

Les fonctions permettant aux applications de contrôler la réflexion (RegDisableReflectionKey et RegEnableReflectionKey) ne sont pas des opérations dans Windows 7.

## <a name="mitigation-of-impact"></a>Atténuation de l’impact

COM est le principal consommateur de la réflexion du Registre. COM et les autres consommateurs ont été mis à jour pour prendre en compte cette modification. Cette modification n’affecte pas les applications qui utilisent des API COM standard.

## <a name="solution"></a>Solution

Appliquez l’une des options suivantes si vous vous fiez à la réflexion du Registre pour synchroniser les vues 32 bits et 64 bits :

-   Créer des clés dans les deux vues explicitement lors de l’installation
-   Déplacer les clés en dehors de l’étendue des clés réfléchies
-   Vérifier les deux vues du registre lors de l’interrogation d’une clé réfléchie

    **Remarque :** \_ \_ Les indicateurs Key WOW64 32KEY et Key \_ WOW64 \_ 64KEY ne peuvent pas être combinés

Appliquez l’une des options suivantes si vous vous fiez aux fonctions RegDisableReflectionKey pour désactiver la réflexion du Registre :

-   Créer des clés dans les deux vues explicitement lors de l’installation
-   Déplacer les clés en dehors de l’étendue des clés réfléchies
-   Utiliser des sous-clés spécifiques à la plateforme (telles que x86, amd64 et ia64) pour séparer les données de bits spécifiques

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Article sur la réflexion du Registre](../winprog64/registry-reflection.md)
-   [Liste des clés redirigées dans l’article redirecteur du Registre](../winprog64/registry-redirector.md)
-   [Meilleures pratiques pour WOW64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
