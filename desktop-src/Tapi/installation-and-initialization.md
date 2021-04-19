---
description: L’installation d’un nouveau fournisseur de services est spécifique aux appareils et au système d’exploitation, donc les détails ne sont pas abordés dans le cadre de ce kit de développement logiciel (SDK).
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installation et initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534736"
---
# <a name="installation-and-initialization"></a>Installation et initialisation

L’installation d’un nouveau fournisseur de services est spécifique aux appareils et au système d’exploitation, donc les détails ne sont pas abordés dans le cadre de ce kit de développement logiciel (SDK). En règle générale, l’objectif de l’installation est la configuration du fournisseur de services pour l’environnement de communication actuel. Cela implique généralement les entrées de Registre et le paramètre des dépendances de service.

L’initialisation d’un fournisseur de services de téléphonie commence par la négociation de version. Consultez [gestion des versions TSPI](tspi-versioning.md) pour une discussion sur la négociation de versions et la version actuelle.

L’interface TAPI appelle ensuite [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), qui transmet au fournisseur un pointeur vers une fonction de rappel utilisée pour signaler la progression des fonctions asynchrones. Le TSP renvoie un nombre de lignes et d’appareils téléphoniques associés à l’identificateur d’appareil actuel.

En règle générale, l’étape suivante est l’inventaire des ressources, effectué par TAPI appelant [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) et [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Le fournisseur de services est supposé remplir les éléments des structures de données impliquées qui se rapportent aux fonctionnalités de l’appareil et de la session qu’il prend en charge.

L’interface TAPI collecte des informations à partir des différentes applications relatives aux exigences de notification d’événement et indique au TSP d’utiliser [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) pour indiquer les types de médias à détecter pour une ligne et [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) pour indiquer les événements de ligne et d’adresse qui doivent être signalés.

 

 
