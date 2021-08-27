---
description: Bien qu’il existe peu de limites techniques quant au type et à la taille des données qu’une application peut stocker dans le registre, certaines recommandations pratiques existent pour favoriser l’efficacité du système.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: espace de Stockage du registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00414edbd34452fd6943a4d73a2ebe85af5d38884ddd0ca77f1d8fb41ae6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885077"
---
# <a name="registry-storage-space"></a>espace de Stockage du registre

Bien qu’il existe peu de limites techniques quant au type et à la taille des données qu’une application peut stocker dans le registre, certaines recommandations pratiques existent pour favoriser l’efficacité du système. Une application doit stocker des données de configuration et d’initialisation dans le registre, et stocker d’autres types de données ailleurs.

En règle générale, les données composées de plus d’un ou de deux kilo-octets (K) doivent être stockées en tant que fichier et référencées à l’aide d’une clé dans le registre plutôt que d’être stockées comme valeur. Au lieu de dupliquer de grands éléments de données dans le registre, une application doit enregistrer les données en tant que fichier et faire référence au fichier. Le code binaire exécutable ne doit jamais être stocké dans le registre.

Une entrée de valeur utilise un espace de registre bien inférieur à celui d’une clé. Pour économiser de l’espace, une application doit regrouper des données similaires en tant que structure et stocker la structure en tant que valeur au lieu de stocker chacun des membres de la structure sous la forme d’une clé distincte. (Le stockage des données sous forme binaire permet à une application de stocker des données en une seule valeur qui serait autrement constituée de plusieurs types incompatibles.)

Les affichages des fichiers du Registre sont mappés dans la mémoire de réserve paginée.

**Windows server 2008 pour 32 bits, Windows vista avec SP1 pour 32 bits, Windows vista, Windows Server 2003, Windows XP :** Les affichages des fichiers du Registre sont mappés dans l’espace d’adressage du cache de l’ordinateur. Par conséquent, quelle que soit la taille des données du Registre, il n’y a pas de facturation supérieure à 4 mégaoctets (Mo).

La taille maximale d’une ruche de Registre est de 2 Go, à l’exception de la ruche système.

**Windows server 2003 avec SP1, Windows server 2003 et Windows XP :** Il n’existe aucune limite explicite quant à la quantité d’espace totale pouvant être consommée par les ruches dans la mémoire de réserve paginée et dans l’espace disque, bien que les quotas système puissent affecter la taille maximale réelle. la taille maximale d’une ruche de registre était limitée à 2 go à partir de Windows Server 2003 avec Service Pack 2 (SP2).

La taille maximale de la ruche système est limitée par la mémoire physique, comme indiqué dans le tableau suivant. 

| Système                      | Taille maximale de la ruche système                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| systèmes basés sur x86           | 50% de la mémoire physique, jusqu’à 400 Mo. **Windows server 2003 avec SP2, Windows server 2003 avec SP1, Windows server 2003 et Windows XP :** 25% de la mémoire physique, jusqu’à 200 mo.<br/>                                    |
| systèmes basés sur x64           | 50% de la mémoire physique, jusqu’à 1,5 Go. **Windows Server 2003 avec SP2 :** 25% de la mémoire système, jusqu’à 200 mo.<br/> **Windows server 2003 avec SP1, Windows server 2003 et Windows XP 64-Bit Edition :** 32 mo.<br/> |
| Systèmes basés sur Intel Itanium | 50% de la mémoire physique, jusqu’à 1 Go. **Windows server 2008, Windows Vista, Windows server 2003 avec SP2, Windows server 2003 avec SP1, Windows server 2003 et Windows XP édition 64 bits :** 32 mo.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

Les données du Registre sont stockées dans la réserve paginée, une zone de mémoire physique utilisée pour les données système qui peuvent être écrites sur le disque quand elles ne sont pas utilisées. La valeur **RegistrySizeLimit** établit la quantité maximale de réserve paginée pouvant être consommée par les données de registre de toutes les applications. Cette valeur se trouve dans la clé de Registre suivante :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

Par défaut, la limite de taille du Registre est de 25% de la réserve paginée. (La taille par défaut de la réserve paginée est de 32 Mo. il s’agit donc de 8 Mo.) Le système vérifie que la valeur minimale de **RegistrySizeLimit** est de 4 Mo et la valeur maximale est environ 80% de la valeur **PagedPoolSize** . Si la valeur de cette entrée est supérieure à 80% de la taille de la réserve paginée, le système définit la taille maximale du Registre à 80% de la taille de la réserve paginée. Cela empêche le registre de consommer l’espace requis par les processus. Notez que la définition de cette valeur n’alloue pas d’espace dans la réserve paginée et ne garantit pas que l’espace sera disponible si nécessaire.

La taille de la réserve paginée est déterminée par la valeur **PagedPoolSize** dans la clé de Registre suivante :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Pour obtenir un exemple de la façon de déterminer la taille actuelle et la taille maximale du Registre, consultez [détermination de la taille du Registre](determining-the-registry-size.md).

La taille maximale de la réserve paginée est d’environ 300 470 Mo, de sorte que la limite de la taille du Registre est de 240-376 Mo. Toutefois, si le commutateur/3GB est utilisé, la taille maximale de la réserve paginée est de 192 Mo, de sorte que le registre peut comporter jusqu’à 153,6 Mo.

 

 




