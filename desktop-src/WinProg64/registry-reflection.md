---
title: Réflexion du Registre
description: Le redirecteur du Registre isole les applications 32 bits et 64 bits en fournissant des vues logiques distinctes de certaines parties du Registre sur WOW64. Toutefois, les valeurs de certaines clés de Registre doivent être identiques dans les vues 32 bits et 64 bits.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- réflexion du Registre, 64 bits, programmation Windows
- la programmation Windows 64 bits de réflexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523041004d9570bbdf101050e30f5d9139031913
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518018"
---
# <a name="registry-reflection"></a>Réflexion du Registre

\[Les informations contenues dans cette rubrique s’appliquent à Windows Server 2008, Windows Vista, Windows Server 2003 et Windows XP. À compter de Windows 7 et de Windows Server 2008 R2, WOW64 n’utilise plus la réflexion du Registre et les clés précédemment réfléchies sont partagées à la place. Pour plus d’informations, consultez [clés de Registre affectées par WOW64](shared-registry-keys.md).\]

Le [redirecteur du Registre](registry-redirector.md) isole les applications 32 bits et 64 bits en fournissant des vues logiques distinctes de certaines parties du Registre sur WOW64. Toutefois, les valeurs de certaines clés de Registre doivent être identiques dans les vues 32 bits et 64 bits.

Le processus de *réflexion du Registre* copie les clés de Registre et les valeurs entre deux vues du Registre pour les maintenir synchronisées. Chaque vue a une copie physique distincte de chaque clé de Registre réfléchie, une pour la vue de Registre 32 bits et l’autre pour la vue de Registre 64 bits.

Une clé réfléchie est copiée quand une clé est fermée en appelant [**échec RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey). Notez que cela donne lieu à une situation de concurrence possible : si plusieurs processus modifient la clé réfléchie, le dernier appel **échec RegCloseKey** détermine la valeur finale de la clé.

Le réflecteur copie les données d’activation COM pour les serveurs locaux entre les vues, mais il ne copie pas les données in-process, car le mixage de données in-process 32/64 n’est pas autorisé sur Windows 64 bits.

La réflexion n’est pas activée pour les clés de Registre partagées ou pour les clés de Registre qui ne sont pas redirigées. Par exemple, la réflexion n’est pas activée pour la clé **\_ \_ \\ système HKEY local machine** . Pour obtenir la liste des clés de Registre qui sont redirigées, partagées ou reflétées, consultez [clés de Registre affectées par WOW64](shared-registry-keys.md).

La réflexion du Registre utilise une stratégie « dernier enregistreur gagne », comme illustré dans l’exemple suivant :

-   Après une nouvelle installation de Windows 64 bits, le Wordpad.exe 64 bits est inscrit pour gérer les fichiers. doc. Le réflecteur copie l’inscription. doc à partir de la vue de Registre 64 bits dans la vue de Registre 32 bits.
-   Un administrateur installe le bureau 32 bits, qui inscrit le Winword.exe 32 bits pour gérer les fichiers. doc dans l’affichage du Registre 32 bits. Le réflecteur du Registre copie ces informations dans la vue de Registre 64 bits, de sorte que les applications 32 bits et 64 bits lancent la version 32 bits de Winword.exe pour les fichiers. doc.
-   Un administrateur installe le bureau 64 bits, qui inscrit le Winword.exe 64 bits pour gérer les fichiers. doc dans l’affichage du Registre 64 bits. Le réflecteur de Registre copie ces informations dans le registre 32 bits, de sorte que les applications 32 bits et 64 bits lancent la version 64 bits de Winword.exe pour les fichiers. doc.

Par conséquent, les informations d’association de fichiers sont conservées pour l’application la plus récemment installée.

Il peut être utile pour les applications 32 bits et 64 bits de partager des valeurs de clé de Registre spécifiques qui sont normalement écrites dans des vues de Registre distinctes. Par exemple, un serveur OLE 32 bits qui peut traiter les demandes des clients 32 bits et 64 bits peut rendre les données de Registre 32 bits disponibles pour la vue 64 bits du Registre système.

Quand un composant écrit des données dans le registre système, WOW64 analyse les informations et effectue une copie des données dans l’autre vue du Registre, le cas échéant. En général, ce processus conserve deux copies physiques distinctes des mêmes clés de Registre dans les deux vues du Registre, et est appelée réflexion du registre ou mise en miroir du Registre.

La plupart des clés sous la racine des classes se trouvent dans cette catégorie. Les mises à jour des clés sont reflétées lorsque la mise à jour est terminée et que le handle de la clé se ferme. Dans certains cas, les écritures dans une clé ne sont pas reflétées si la clé a une dépendance de nombre de bits. Par exemple, la clé InprocServer32 32 bits n’est pas pertinente pour les applications 64 bits, donc la clé InprocServer32 n’est pas reflétée dans la vue de Registre 64 bits. Toutefois, les applications 64 bits peuvent utiliser la clé LocalServer32 de 32 bits et la clé LocalServer32 est reflétée.

Pour **les \_ classes de logiciel HKEY local \_ machine \\ \\ \\ CLSID** et **HKEY \_ Current \_ User \\ Software \\ classes \\ CLSID**, seuls les CLSID qui ne spécifient pas InprocServer32 ou InprocHandler32 sont reflétés. Seuls les CLSID LocalServer32 sont reflétés, car ils s’exécutent hors processus et peuvent être activés par des applications 32 ou 64 bits. Les CLSID InProcServer32 ne sont pas reflétés, car il n’est pas possible de charger une DLL 32 bits pour l’exécution dans un processus 64 bits, ou une DLL 64 bits pour l’exécution dans un processus de 32 bits.

Pour les classes de logiciels de la classe HKEY de l' **\_ \_ ordinateur local \\ \\ \\ AppID** et **HKEY \_ Current \_ User \\ Software \\ classes \\ AppID**, les valeurs de Registre [DllSurrogate](../com/dllsurrogate.md) et [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) ne sont pas reflétées si leur valeur est une chaîne vide.

Pour désactiver et activer la réflexion du Registre pour une clé réfléchie particulière, utilisez les fonctions [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) et [**RegEnableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) . Ces fonctions n’affectent pas les clés qui ne figurent pas dans la liste des clés réfléchies, plus haut dans cette rubrique. Les applications doivent désactiver la réflexion uniquement pour les clés de registre qu’elles créent et ne pas tenter de désactiver la réflexion pour les clés prédéfinies, telles que **HKEY \_ local \_ machine** ou **HKEY \_ Current \_ User**. Pour déterminer si les clés de la liste de réflexion ont été désactivées, utilisez la fonction [**RegQueryReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey) .

Les clés réfléchies ne doivent pas être utilisées dans les opérations de Registre traitées. L’écriture de clés reflétées pendant une transaction peut provoquer l’échec de la transaction. Pour plus d’informations sur les transactions, consultez [Gestionnaire de transactions du noyau](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Redirecteur du Registre](registry-redirector.md)
</dt> <dt>

[Réflexion du Registre dans Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Clés de Registre affectées par WOW64](shared-registry-keys.md)
</dt> </dl>

 

 