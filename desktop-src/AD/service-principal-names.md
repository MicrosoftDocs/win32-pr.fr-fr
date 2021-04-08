---
title: Noms des principaux du service
description: Un nom de principal du service (SPN) est un identificateur unique d’une instance de service.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Noms des principaux du service
- SPN voir noms de principal du service
- nom de principal du service AD
- nom de principal du service AD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842022"
---
# <a name="service-principal-names"></a>Noms des principaux du service

Un nom de principal du service (SPN) est un identificateur unique d’une instance de service. Les SPN sont utilisés par [l’authentification Kerberos](mutual-authentication-using-kerberos.md) pour associer une instance de service à un compte d’ouverture de session de service. Cela permet à une application cliente de demander que le service authentifie un compte même si le client n’a pas le nom du compte.

Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN. Une instance de service donnée peut posséder plusieurs noms SPN si les clients peuvent utiliser plusieurs noms pour l'authentification. Par exemple, un nom de principal du service (SPN) comprend toujours le nom de l’ordinateur hôte sur lequel l’instance de service s’exécute, de sorte qu’une instance de service peut inscrire un SPN pour chaque nom ou alias de son hôte. Pour plus d’informations sur le format SPN et la composition d’un nom principal de service unique, consultez [formats de noms pour les noms de principal du service uniques](name-formats-for-unique-spns.md).

Avant que le service d’authentification Kerberos puisse utiliser un nom de principal du service pour authentifier un service, le SPN doit être inscrit sur l’objet de compte utilisé par l’instance de service pour ouvrir une session. Un SPN donné peut être inscrit sur un seul compte. Pour les services Win32, un programme d’installation de service spécifie le compte d’ouverture de session lorsqu’une instance du service est installée. Le programme d’installation compose ensuite les noms de principal du service et les écrit en tant que propriété de l’objet de compte dans Active Directory Domain Services. Si le compte d’ouverture de session d’une instance de service change, les SPN doivent être réinscrits sous le nouveau compte. Pour plus d’informations, consultez [Comment un service enregistre ses SPN](how-a-service-registers-its-spns.md).

Pour se connecter à un service, le client localise une instance du service, compose le nom principal du service pour cette instance, se connecte au service et présente le nom principal de service pour que le service s'authentifie. Pour plus d’informations, consultez [Comment les clients composent le SPN d’un service](how-clients-compose-a-serviceampaposs-spn.md).

## <a name="in-this-section"></a>Dans cette section

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Formats de noms pour les SPN uniques](name-formats-for-unique-spns.md)
</dt> <dt>

[Comment un service compose ses SPN](how-a-service-composes-its-spns.md)
</dt> <dt>

[Comment un service enregistre ses SPN](how-a-service-registers-its-spns.md)
</dt> <dt>

[Comment les clients composent le SPN d’un service](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Qu’est-ce qu’un SPN et Pourquoi devez-vous vous en soucier ?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Authentification mutuelle à l'aide de Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 