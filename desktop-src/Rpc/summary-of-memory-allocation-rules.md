---
title: Résumé des règles d’allocation de mémoire
description: Le tableau suivant récapitule les principales règles relatives à l’allocation de mémoire.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102008"
---
# <a name="summary-of-memory-allocation-rules"></a>Résumé des règles d’allocation de mémoire

Le tableau suivant récapitule les principales règles relatives à l’allocation de mémoire.



| Élément MIDL                                                                                                                                           | Description                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pointeurs de \[ [référence](/windows/desktop/Midl/ref) de niveau supérieur \]                                                                                                                | Il doit s’agir de pointeurs non null.                                                                                                                                            |
| Valeur de retour de la fonction                                                                                                                                  | La nouvelle mémoire est toujours allouée pour les valeurs de retour de pointeur.                                                                                                             |
| \[pointeur [unique](/windows/desktop/Midl/unique), de [sortie](/windows/desktop/Midl/out-idl) \] ou \[ [ptr](/windows/desktop/Midl/ptr), point de sortie \]                                                                   | Non autorisé par MIDL.                                                                                                                                                  |
| Pointeur non-de niveau \[ [supérieur](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] ou \[ [ptr](/windows/desktop/Midl/ptr), in, out \] qui passe de null à non null | Les stubs client allouent une nouvelle mémoire sur le client au retour.                                                                                                                 |
| \[Pointeur de [sortie](/windows/desktop/Midl/out-idl) [unique](/windows/desktop/Midl/unique), [de](/windows/desktop/Midl/in)niveau non supérieur, \] qui change de non null en null                                 | La mémoire est orpheline sur le client ; l’application cliente est chargée de libérer de la mémoire et d’éviter les fuites.                                                              |
| \[Pointeur de sortie [ptr](/windows/desktop/Midl/ptr), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) de niveau supérieur \] qui passe de non null à null                                       | La mémoire sera orpheline sur le client s’il n’a pas d’alias ; dans ce cas, l’application cliente est chargée de libérer et d’éviter les fuites de mémoire.                             |
| \[[référence](/windows/desktop/Midl/ref) \] pointeurs                                                                                                                           | Client-la couche application est généralement allouée.                                                                                                                           |
| Pointeur non null \[ [dans](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \]                                                                                                | Les stubs essaient d’écrire dans le stockage existant sur le client. Si la taille de **\[ chaîne \]** et de taille augmente au-delà de la taille allouée sur le client, elle provoque une erreur GP au retour. |



 

Le tableau suivant récapitule les effets des attributs IDL de clé et ACF sur la gestion de la mémoire.



| Fonctionnalité MIDL                                                                   | Problèmes de clients                                                                                                                                  | Problèmes de serveur                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[allocate](/windows/desktop/Midl/allocate)( \_ nœud unique) \] , \[ allocate (tous les \_ nœuds)\]         | Détermine si un ou plusieurs appels sont effectués aux fonctions de mémoire.                                                                         | Identique au client, à la différence que la mémoire privée peut souvent être utilisée pour l’allocation ( \_ nœud unique) \[ dans \] et \[ dans, les données de sortie \] .               |
| \[allouer (gratuit) \] ou \[ allouer (ne pas \_ libérer)\]                                 | (Aucune ; affecte le serveur.)                                                                                                                        | Détermine si la mémoire sur le serveur est libérée après chaque appel de procédure distante.                                            |
| les attributs \[ de tableau [Max \_ sont](/windows/desktop/Midl/max-is) \] et \[ [size \_ est](/windows/desktop/Midl/size-is)\] | (Aucune ; affecte le serveur.)                                                                                                                        | Détermine la taille de la mémoire à allouer.                                                                                    |
| \[[ \_ nombre d’octets](/windows/desktop/Midl/byte-count)\]                                            | Le client doit allouer la mémoire tampon ; non alloué ou libéré par les stubs client.                                                                           | L’attribut de paramètre ACF détermine la taille de la mémoire tampon allouée sur le serveur.                                                        |
| \[[activer l' \_ allocation](/windows/desktop/Midl/enable-allocate)\]                                  | En général, aucun. Toutefois, le client peut utiliser un autre environnement de gestion de la mémoire.                                                     | Le serveur utilise un autre environnement de gestion de la mémoire. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) doit être utilisé pour les allocations. |
| \[[dans](/windows/desktop/Midl/in) \] attribut                                                    | Application cliente chargée d’allouer de la mémoire pour les données.                                                                                 | Alloué sur le serveur par stubs.                                                                                                 |
| \[en [sortie](/windows/desktop/Midl/out-idl) \] attribut                                             | Alloué sur le client par stubs.                                                                                                                  | \[en [sortie](/windows/desktop/Midl/out-idl) \] -seul le pointeur doit être un \[ [](/windows/desktop/Midl/ref) \] pointeur Ref ; alloué sur le serveur par stubs.                       |
| \[[référence](/windows/desktop/Midl/ref) \] attribut                                                 | La mémoire référencée par le pointeur doit être allouée par l’application cliente.                                                                          | Pointeurs de référence de niveau supérieur et de premier niveau gérés par des stubs.                                                                |
| \[[unique](/windows/desktop/Midl/unique) \] attribut                                           | Une valeur non null pour null peut entraîner une mémoire orpheline ; NULL avec une valeur non null provoque l’appel par le stub client pour appeler l' [ \_ \_ allocation d’utilisateur MIDL](/windows/desktop/Midl/midl-user-allocate-1). | (Affecte le client.)                                                                                                             |
| \[[pointeur](/windows/desktop/Midl/ptr) \] attribut                                                 | (Voir \[ [unique](/windows/desktop/Midl/unique) \] .)                                                                                                              | (Voir \[ [unique](/windows/desktop/Midl/unique) \] .)                                                                                             |



 

 

 