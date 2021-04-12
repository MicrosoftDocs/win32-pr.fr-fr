---
description: La \_ \_ liste d’adresses SIO \_ trie IOCTL permet aux développeurs d’applications de trier une liste d’adresses de destination IPv6 et IPv4 pour déterminer la meilleure adresse disponible pour établir une connexion. La \_ \_ liste d’adresses SIO \_ Tri IOCTL est prise en charge sur Windows XP et versions ultérieures.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Utilisation de SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210227"
---
# <a name="using-sio_address_list_sort"></a>Utilisation du \_ \_ tri de liste d’adresses SIO \_

La **\_ liste d’adresses SIO \_ \_ trie** IOCTL permet aux développeurs d’applications de trier une liste d’adresses de destination IPv6 et IPv4 pour déterminer la meilleure adresse disponible pour établir une connexion. La **\_ liste d’adresses SIO \_ \_ Tri** IOCTL est prise en charge sur Windows XP et versions ultérieures.

Sur Windows Vista et versions ultérieures, la fonction [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) prend la liste fournie d’adresses de destination IP potentielles, associe les adresses de destination aux adresses IP locales de l’ordinateur hôte et trie les paires en fonction de la meilleure correspondance d’adresse pour les communications entre les deux pairs. La fonction **CreateSortedAddressPairs** doit être utilisée à la place de la **liste d’adresses SIO \_ \_ \_ Tri** IOCTL sur Windows Vista et versions ultérieures.

Les sections suivantes décrivent les considérations relatives à l’utilisation du **\_ tri de \_ liste \_ d’adresses SIO**.

## <a name="parameters"></a>Paramètres

La mémoire tampon transmise à **SIO \_ address \_ List \_ sort** est une structure de [**\_ \_ liste d’adresses de sockets**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) . Chaque [**\_ adresse de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) de la liste doit être au \_ format sockaddr in6.

La **\_ liste d’adresses SIO \_ \_ Trier** IOCTL trie les adresses IPv6 et IPv4 sur Windows Vista et versions ultérieures. Toutes les adresses IPv4 de la liste à trier doivent être au format d’adresse IPv6 mappé IPv4. Pour plus d’informations sur le format d’adresse IPv6 mappée IPv4, consultez [sockets à double pile](dual-stack-sockets.md).

Sur Windows Server 2003 et Windows XP, le **tri de la \_ \_ liste \_ d’adresses SIO** trie uniquement les adresses IPv6. Les adresses IPv4 dans le format d’adresse IPv6 mappée IPv4 ne sont pas prises en charge.

Lors de la sortie, le membre **iAddressCount** de la structure de [**liste d' \_ adresses \_ de sockets**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) peut être plus petit que en entrée si le code IOCTL détermine que certaines adresses de destination ne sont pas valides.

## <a name="sorting-determination"></a>Détermination du tri

L’ordre de tri des adresses IPv6 pour le \_ tri de la liste d’adresses SIO \_ \_ est basé sur la table de stratégie de préfixe. La table de stratégie de préfixe est configurée à l’aide de l’utilitaire de ligne de commande *Netsh.exe* . Les extraits de ligne de commande suivants illustrent les commandes de configuration de la table de préfixe *Netsh.exe* de base :

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> Sur Windows Server 2003 et Windows XP, la première commande netsh listée ci-dessus était la suivante. Toutes les autres commandes associées sont identiques.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

Le classement des adresses est également déterminé par un algorithme décrit dans le document RFC 3484 sur la *sélection d’adresses par défaut pour le protocole IPv6 (Internet Protocol version 6)* publié par l’IETF. Pour plus d’informations, consultez [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). (Cette ressource peut uniquement être disponible en anglais.)

La **\_ liste d’adresses SIO \_ \_ sort** d’IOCTL trie les adresses du meilleur au pire, et renseigne les membres de l' **\_ \_ ID d’étendue Sin6** , si nécessaire. Pour les adresses locales de site, le tri de la \_ liste d’adresses SIO \_ \_ peut remplir l’ID de l’étendue ou supprimer l’adresse.

La **\_ liste d’adresses SIO \_ \_ Tri** IOCTL ignore l’adresse source liée au socket et trie uniquement en fonction de la liste d’adresses de destination transmise en tant que paramètre.

La fonction [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) doit être utilisée à la place de la **liste d’adresses SIO \_ \_ \_ Tri** IOCTL sur Windows Vista et versions ultérieures. La fonction **CreateSortedAddressPairs** retourne une liste de paires d’adresses qui contient une adresse source locale et une adresse de destination. Cela fournit à une application l’adresse source appropriée à utiliser pour chaque adresse de destination. Une application peut également filtrer les résultats en recherchant une adresse source spécifique. dans les résultats.

## <a name="requirements"></a>Configuration requise

La **liste d’adresses SIO de \_ \_ \_ Tri** IOCTL est définie dans le fichier d’en-tête *Winsock2. h* . Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et **SIO \_ address \_ List \_ Tri** IOCTL est défini dans le fichier d’en-tête *Ws2def. h* . Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.

La **\_ liste d’adresses SIO \_ \_ Tri** IOCTL est prise en charge sur Windows XP et versions ultérieures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
