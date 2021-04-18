---
description: Pour qu’un fournisseur d’espace de noms soit accessible via Windows Sockets, il doit être correctement installé sur le système et enregistré auprès de Windows Sockets.
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: Configuration et installation de la résolution de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e0ca7c9c5290a040a17e0f1ded2a97a1aed15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516243"
---
# <a name="name-resolution-configuration-and-installation"></a>Configuration et installation de la résolution de noms

Pour qu’un fournisseur d’espace de noms soit accessible via Windows Sockets, il doit être correctement installé sur le système et enregistré auprès de Windows Sockets. Lorsqu’un fournisseur d’espace de noms est installé en appelant le programme d’installation d’un fournisseur, les informations de configuration doivent être ajoutées à une base de données de configuration pour fournir au \_ service Ws232.dll informations nécessaires concernant le fournisseur de services. L' \_32.dll Ws2 exporte [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) pour le programme d’installation du fournisseur à utiliser. Cette fonction est utilisée pour fournir des informations pertinentes sur le fournisseur de services à installer. Ces informations incluent :

-   Nom du fournisseur : chaîne représentant le fournisseur à afficher dans le panneau de configuration.
-   Version du fournisseur : version de ce fournisseur.
-   Chemin d’accès du fournisseur : nom de chemin d’accès à la DLL du fournisseur.
-   Espace de noms : espace de noms pris en charge par le fournisseur.
-   GUID du fournisseur : nombre unique fourni par le fournisseur représentant cette combinaison fournisseur/espace de noms. Elle est utilisée comme clé pour toutes les références ultérieures à ce fournisseur, et pour la désinstallation. Ces valeurs sont créées à l’aide de l’utilitaire Uuidgen.exe.
-   Stocke tous les indicateurs (un indicateur qui spécifie si ce fournisseur d’espace de noms est chargé de conserver toutes les informations de schéma de la classe de service pour toutes les classes de service). Si un tel fournisseur existe, le \_32.dll Ws2 n’a pas besoin d’interroger chaque fournisseur d’espace de noms pour obtenir ces informations.

Sur Windows Vista et versions ultérieures, une fonction [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) améliorée est fournie pour permettre au fournisseur d’espace de noms de passer un objet blob de données supplémentaire spécifique à l’espace de noms.

Sur les plateformes 64 bits, les fonctions [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) et [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) similaires sont fournies pour installer un espace de noms dans le catalogue 32 bits.

Le \_32.dll Ws2 fournit également une fonction, [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace), pour le programme de désinstallation d’un fournisseur afin de supprimer toutes les informations pertinentes de la base de données de configuration. L’emplacement et le format exacts de ces informations de configuration sont privés pour le \_32.dll Ws2 et ne peuvent être manipulés que par les fonctions mentionnées ci-dessus.

Sur les plateformes 64 bits, une fonction [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) similaire est fournie pour désinstaller un espace de noms dans le catalogue 32 bits.

À tout moment, un fournisseur d’espace de noms est considéré comme actif ou inactif, avec ce paramètre contrôlé via les fonctions [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) et [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) . Les fournisseurs d’espaces de noms qui sont inactifs continuent à s’afficher lorsqu’ils sont énumérés (à l’aide des fonctions [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa), [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa), [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)et [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) ), mais le32.dll Ws2 n' \_ achemine pas les opérations d’inscription de requête ou de service à ces fournisseurs. Cette fonctionnalité peut être utile dans les situations où plusieurs fournisseurs d’espaces de noms installés peuvent prendre en charge un espace de noms donné.

Lorsque plusieurs fournisseurs d’espaces de noms sont référencés dans une seule fonction d’API, l’ordre dans lequel l’ordre dans lequel les requêtes et les opérations d’enregistrement sont routées vers les fournisseurs d’espaces de noms n’est pas spécifié. L’ordre n’est pas lié à l’ordre dans lequel les fournisseurs d’espaces de noms sont installés. Il existe deux façons de contrôler les fournisseurs d’espaces de noms qui sont utilisés pour résoudre une requête de nom. Tout d’abord, les fonctions [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) et [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) peuvent être utilisées pour activer et désactiver des espaces de noms à l’ensemble de l’ordinateur et de façon permanente. Deuxièmement, les applications peuvent diriger une requête individuelle vers un fournisseur particulier en spécifiant le GUID d’identification de ce fournisseur dans le cadre de la requête.

 

 



