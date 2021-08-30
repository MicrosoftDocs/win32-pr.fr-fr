---
description: à partir de Windows Server 2003, le groupe utilisateurs de l’analyseur de performances et le groupe utilisateurs du journal des performances ont été mis à la disposition des développeurs et des utilisateurs des dll de performances et des fonctions de l’API d’assistance des données de performances (PDH).
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: Restriction de l’accès aux DLL d’extension de performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43bfe7877a3ab93ea21945eacd9398d9f9536deff66ca9bd95b73abea7d8d1aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962379"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>Restriction de l’accès aux DLL d’extension de performance

à partir de Windows Server 2003, le groupe utilisateurs de l’analyseur de performances et le groupe utilisateurs du journal des performances ont été mis à la disposition des développeurs et des utilisateurs des dll de performances et des fonctions de l’API d’assistance des données de performances (PDH). Ces groupes de sécurité des performances sont destinés à être utilisés par les administrateurs système pour limiter l’accès aux informations exposées par les dll de performance à une liste spécifique d’utilisateurs.

Le groupe utilisateurs de l’analyseur de performances est destiné à inclure les utilisateurs qui affichent les données des compteurs et n’enregistre pas les données des compteurs à l’aide du service Journaux et alertes de performance. Le groupe utilisateurs du journal de performances doit inclure des utilisateurs qui ont l’autorisation d’utiliser les journaux de performances et le service d’alerte pour enregistrer les compteurs sur le serveur local ou distant. Les privilèges de ce groupe incluent également la création de fichiers journaux sur des systèmes locaux ou distants, l’utilisation du service d’alertes et l’exécution de programmes dans le cadre du service.

Notez que ces groupes de sécurité de performance ne sont pas eux-mêmes un mécanisme de restriction d’accès. pour ce faire, vous devez utiliser ces groupes avec le modèle de contrôle d’accès aux objets Windows.

La plupart des applications communiquent avec la DLL de performance via un mécanisme IPC, en général la mémoire partagée. Par conséquent, vous pouvez ajouter les membres d’un groupe de sécurité de performances au descripteur de sécurité de l’objet de mémoire partagée pour limiter l’accès à la DLL aux membres du groupe de sécurité. Dans ce cas, vous devez également ajouter les membres du groupe au descripteur de sécurité des objets système auxquels la DLL de performance accède pour fournir des données de compteur, par exemple, des fichiers journaux et des dossiers. Pour plus d’informations sur l’ajout de listes de contrôle d’accès aux descripteurs de sécurité des objets, consultez Modification de l' [ACL d’un objet](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--).

Une autre méthode que vous pouvez utiliser pour modifier les informations de liste de contrôle d’accès du descripteur de sécurité d’un objet système IPC consiste à spécifier les membres de la liste de groupes de sécurité des performances avec le langage SDDL (Security Descriptor Definition Language) et à appeler [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) pour créer le descripteur de sécurité. Ce descripteur de sécurité est ensuite attaché à l’objet système IPC. L’exemple suivant illustre une chaîne SDDL qui comprend le groupe utilisateurs de l’analyseur de performances, MU et le groupe utilisateurs du journal des performances, LU.

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
