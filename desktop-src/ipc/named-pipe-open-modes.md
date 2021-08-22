---
description: Le serveur de canal spécifie les modes d’accès, de chevauchement et d’écriture dans le canal dans le paramètre dwOpenMode de la fonction CreateNamedPipe. Les clients de canal peuvent spécifier ces modes ouverts pour leurs handles de canal à l’aide de la fonction CreateFile.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Modes ouverts du canal nommé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7fe3f843a157e69d8b938630e5eb9efa95035960cb6578325be6bddd5d93c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451259"
---
# <a name="named-pipe-open-modes"></a>Modes ouverts du canal nommé

Le serveur de canal spécifie les modes d’accès, de chevauchement et d’écriture dans le canal dans le paramètre *dwOpenMode* de la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Les clients de canal peuvent spécifier ces modes ouverts pour leurs handles de canal à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="access-mode"></a>Mode d’accès

La définition du mode d’accès au canal revient à spécifier l’accès en lecture ou en écriture associé aux descripteurs du serveur de canal. Le tableau suivant indique le droit d’accès générique équivalent pour chaque mode d’accès que vous pouvez spécifier avec [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).



| Mode d’accès            | Droit d’accès générique équivalent |
|------------------------|---------------------------------|
| \_accès au canal \_ entrant  | \_lecture générique                   |
| \_accès au canal \_ sortant | \_écriture générique                  |
| \_duplex d’accès du canal \_   | \_écriture générique en lecture générique \| \_ |



 

Si le serveur de canal crée un canal avec \_ accès au canal \_ entrant, le canal est en lecture seule pour le serveur de canal et en écriture seule pour le client de canal. Si le serveur de canaux crée un canal avec \_ accès aux canaux \_ sortant, le canal est en écriture seule pour le serveur de canal et en lecture seule pour le client de canal. Un canal créé avec le \_ duplex d’accès \_ de canal est en lecture/écriture pour le serveur de canaux et le client de canal.

Les clients de canal utilisant [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour se connecter à un canal nommé doivent spécifier un droit d’accès dans le paramètre *dwDesiredAccess* qui est compatible avec le mode d’accès spécifié par le serveur de canaux. Par exemple, un client doit spécifier un \_ accès en lecture générique pour ouvrir un handle pour un canal que le serveur de canal a créé avec l' \_ accès au canal \_ sortant. Les modes d’accès doivent être les mêmes pour toutes les instances d’un canal.

Pour lire des attributs de canal tels que le mode lecture ou le mode blocage, le handle de canal doit avoir les attributs de lecture de fichier \_ \_ droits d’accès ; pour écrire des attributs de canal, le handle de canal doit avoir le \_ droit d’accès écriture de fichier \_ . Ces droits d’accès peuvent être combinés avec le droit d’accès générique qui est approprié pour le canal : \_ lecture générique \_ avec \_ attributs d’écriture de fichier pour un canal en lecture seule, ou \_ écriture générique avec \_ \_ attributs de lecture de fichier pour un canal en écriture seule. La restriction des droits d’accès de cette façon offre une meilleure sécurité pour le canal.

## <a name="overlapped-mode"></a>Mode avec chevauchement

En mode avec chevauchement, les fonctions qui effectuent des opérations de lecture, d’écriture et de connexion longues peuvent être immédiatement retournées. Cela permet au thread d’effectuer d’autres opérations pendant qu’une opération qui prend du temps s’exécute en arrière-plan. Pour spécifier le mode avec chevauchement, utilisez l' \_ indicateur de chevauchement de l’indicateur de fichier \_ . Pour plus d’informations, consultez [entrées et sorties synchrones et avec chevauchement](synchronous-and-overlapped-input-and-output.md).

La fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permet au client de canal de définir le mode Overlapped (avec \_ indicateur \_ de fichier Overlapped) pour ses handles de canal à l’aide du paramètre *dwFlagsAndAttributes* .

## <a name="write-through-mode"></a>Mode de Write-Through

Spécifiez le mode écriture à l’aide d’un indicateur de fichier en \_ \_ écriture \_ . Ce mode affecte uniquement les opérations d’écriture aux canaux de type octet entre les clients de canal et les serveurs de canal sur des ordinateurs différents. En mode écriture, les fonctions qui écrivent dans un canal nommé ne sont pas retournées tant que les données ne sont pas transmises sur le réseau et dans la mémoire tampon du canal sur l’ordinateur distant. Le mode écriture est utile pour les applications qui nécessitent une synchronisation pour chaque opération d’écriture.

Si le mode d’écriture n’est pas activé, le système améliore l’efficacité des opérations réseau en passant les données en mémoire tampon jusqu’à ce que le nombre minimal d’octets soit écoulé ou jusqu’à ce qu’un laps de temps maximal soit écoulé. La mise en mémoire tampon permet au système de combiner plusieurs opérations d’écriture dans une seule transmission réseau. Cela signifie qu’une opération d’écriture peut être effectuée correctement après que le système a placé les données dans la mémoire tampon sortante, mais avant que le système ne les transmette sur le réseau.

La fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) permet au client de canal de définir le mode d’écriture (l’indicateur de fichier en \_ \_ écriture \_ ) pour ses descripteurs de canal à l’aide du paramètre *dwFlagsAndAttributes* . Le mode d’écriture directe d’un handle de canal ne peut pas être modifié après la création du handle de canal. Le mode d’écriture peut être différent pour les handles de serveur et de client vers la même instance de canal.

Un client de canal peut utiliser la fonction [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) pour contrôler le nombre d’octets et le délai d’attente avant la transmission d’un canal sur lequel le mode d’écriture est désactivé. Pour un canal en lecture seule, le descripteur de canal doit être ouvert avec les \_ droits d’accès de lecture et d’écriture de fichier génériques \_ \_ .

 

 
