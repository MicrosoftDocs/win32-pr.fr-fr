---
title: Recherche et chargement des ressources
description: Cette rubrique explique comment charger une ressource en mémoire.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b2a66628e5cdceb485df315dc27f0189fe23decbb6205e76d97f3afb77a380
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886799"
---
# <a name="finding-and-loading-resources"></a>Recherche et chargement des ressources

Avant d’utiliser une ressource, une application doit la charger en mémoire. Les fonctions [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) et [**FindResourceEx**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) recherchent une ressource dans un module et retournent un descripteur aux données de ressource binaires. **FindResource** localise une ressource par type et par nom. **FindResourceEx** localise la ressource par type, nom et langue. Les informations sur **FindResource** dans cette rubrique s’appliquent également à **FindResourceEx**.

La fonction [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) utilise le handle de ressource retourné par [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) pour charger la ressource en mémoire. Une fois qu’une application a chargé une ressource à l’aide de **LoadResource**, le système décharge la mémoire associée uniquement lorsque toutes les références à son module sont libérées via [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Les applications qui doivent accéder à plusieurs fois au même ou à de nombreuses ressources au sein d’un module particulier peuvent entraîner des pénalités en matière de performances, car le mappage de mémoire a lieu dans les appels [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et **FreeLibrary** répétés. Les applications doivent stocker un handle de module unique jusqu’à ce que les ressources ne soient plus nécessaires, puis appeler **FreeLibrary**. Une fois qu’un module est déchargé de la mémoire, les handles de ressource deviennent non valides.

Une application peut utiliser [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) et [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) pour rechercher et charger n’importe quel type de ressource, mais ces fonctions ne doivent être utilisées que dans l’une des situations suivantes :

-   Lorsque l’application ne peut pas accéder à la ressource à l’aide d’une fonction existante spécifique à une ressource.
-   Lorsque l’application doit accéder à la ressource en tant que données binaires pour les appels de fonction suivants.

Dans la mesure du possible, une application doit utiliser l’une des fonctions spécifiques aux ressources suivantes pour rechercher et charger des ressources dans un appel :



| Fonction                                     | Action                                   | Pour supprimer une ressource                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Charge et met en forme une entrée de table de messages. | Aucune action n'est nécessaire.                                                                                                |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Charge une table d’accélérateurs.              | [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Charge une ressource bitmap.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Charge une ressource de curseur.                 | [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Charge une ressource icône.                  | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Charge une icône, un curseur ou une bitmap.        | [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**SupprimerObjet**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Charge une ressource de menu.                   | [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Charge une entrée de table de chaînes.              | Aucune action n'est nécessaire.                                                                                                |



 

Notez les fonctions de publication dans le tableau ci-dessus. Avant de se terminer, une application doit libérer la mémoire occupée par les tables, les bitmaps, les curseurs, les icônes et les menus d’accélérateur à l’aide des fonctions appropriées.

La mémoire associée aux ressources chargées via [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) et [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) est libérée une fois que le module a été déchargé par un appel à [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Toutes les ressources qui restent déchargées lors de l’arrêt de l’application sont automatiquement publiées par le système.

 

 