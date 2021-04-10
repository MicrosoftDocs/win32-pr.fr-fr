---
description: Une fois que vous avez récupéré les informations d’installation à partir d’un fichier INF, vous pouvez utiliser plusieurs fonctions de gestion de fichiers pour installer les fichiers répertoriés dans une section INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Installation à partir d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc3642edfb7abc2864c2c0784c79fbb21612fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866937"
---
# <a name="installing-from-an-inf-file"></a>Installation à partir d’un fichier INF

Une fois que vous avez récupéré les informations d’installation à partir d’un fichier INF, vous pouvez utiliser plusieurs fonctions de gestion de fichiers pour installer les fichiers répertoriés dans une section INF. Les fonctions de bas niveau, telles que [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) et [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) , installent un fichier unique.

Il existe également des fonctions pour gérer des fichiers compressés. La fonction [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) retourne des informations sur les fichiers compressés. Ces informations peuvent ensuite être utilisées par [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) pour copier et, si nécessaire, développer le fichier.

Les fonctions de haut niveau telles que [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)et [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) traitent les opérations d’installation dans une section d' **installation** ou de **service** . **SetupInstallFromInfSection** est le plus polyvalent, car il peut effectuer n’importe quel type d’opération d’installation figurant dans la section d' **installation** d’un fichier INF. Cela comprend les opérations de Registre et INI énumérées dans les lignes **AddReg**, **DelReg**, **UpdateInis** ou **UpdateIniField** d’une section d' **installation** .

Les fonctions [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) et [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) défilent les opérations d’une section **installation** ou **service** , respectivement, vers une file d’attente de fichiers existante. Notez que vous devez appeler SetupInstallFromInfSection et SetupInstallServicesFromInfSection séparément pour les opérations de file d’attente et les services. Pour plus d’informations, consultez [files d’attente de fichiers](file-queues.md).

En revanche, la fonction [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crée et détruit sa propre file d’attente interne. Une utilisation courante de **SetupInstallFromInfSection** consiste à l’appeler une fois que tous les fichiers ont été correctement copiés pour effectuer les transactions de Registre et ini.

Sur Windows 2000, les fichiers DLL peuvent être enregistrés automatiquement en appelant [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) sur un fichier INF qui comprend la directive **RegisterDlls** dans sa section d' **installation** . **SetupInstallFromInfSection** peut également inscrire automatiquement des dll 32 bits à partir d’un processus 64 bits.

Sur les systèmes d’exploitation 64 bits, [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) peut être appelé pour effectuer des opérations sur la partie 32 bits du Registre. Pour ajouter une clé de Registre à la partie 32 bits du Registre, incluez l' \_ indicateur FLG ADDREG \_ 32BITKEY dans la ligne **ADDREG** du fichier INF. Pour supprimer une clé de Registre uniquement dans la partie 32 bits du Registre, incluez la \_ clé FLG DELREG \_ 32BITKEY dans la ligne **DelReg** . Pour définir ou effacer une valeur binaire uniquement dans la partie 32 bits du Registre, incluez le \_ 32BITKEY BITREG FLG \_ dans la ligne **BITREG** .

Outre les fonctions mentionnées précédemment, l’API d’installation comprend des fonctions qui défilent les opérations d’installation de fichier, par fichier ou par section INF. Pour plus d’informations, consultez [files d’attente de fichiers](file-queues.md).

 

 



