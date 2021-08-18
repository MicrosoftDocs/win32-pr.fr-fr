---
title: Utilisation du compte LocalSystem en tant que compte d’ouverture de session du service
description: L’un des avantages de l’exécution sous le compte LocalSystem est que le service dispose d’un accès illimité aux ressources locales.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- compte LocalSystem
- LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ac31cb7b3e0ad335f9a2781187aadcb03a1529055eb0771856aa01543add0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024577"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Utilisation du compte LocalSystem en tant que compte d’ouverture de session du service

L’un des avantages de l’exécution sous le compte LocalSystem est que le service dispose d’un accès illimité aux ressources locales. Il s’agit également de l’inconvénient de LocalSystem, car un service LocalSystem peut effectuer des opérations qui pourraient entraîner une baisse de l’ensemble du système. En particulier, un service qui s’exécute en tant que LocalSystem sur un contrôleur de domaine dispose d’un accès illimité à Active Directory Domain Services. Cela signifie que les bogues dans le service, ou les attaques de sécurité sur le service, peuvent endommager le système ou, si le service est sur un contrôleur de réseau, endommager l’ensemble du réseau de l’entreprise.

Pour ces raisons, les administrateurs de domaine des installations sensibles feront attention à ce que les services s’exécutent en tant que LocalSystem. En fait, ils peuvent posséder des stratégies, en particulier sur les contrôleurs de service. Si votre service doit s’exécuter en tant que LocalSystem, la documentation de votre service doit justifier aux administrateurs de domaine les raisons pour lesquelles le service peut être exécuté avec des privilèges élevés. Les services ne doivent jamais s’exécuter en tant que LocalSystem sur un contrôleur de domaine. Pour plus d’informations et pour obtenir un exemple de code qui montre comment un programme d’installation de service ou de service peut déterminer s’il s’exécute sur un contrôleur de domaine, consultez [test de l’exécution de sur un contrôleur de domaine](testing-whether-running-on-a-domain-controller.md).

Lorsqu’un service s’exécute sous le compte LocalSystem sur un ordinateur qui est membre d’un domaine, le service dispose de l’accès réseau accordé au compte d’ordinateur, ou à tous les groupes dont le compte d’ordinateur est membre. sachez que dans Windows 2000, un compte d’ordinateur de domaine est un principal de service, similaire à un compte d’utilisateur. Cela signifie qu’un compte d’ordinateur peut être dans un groupe de sécurité et qu’une entrée du contrôle d’accès dans un descripteur de sécurité peut accorder l’accès à un compte d’ordinateur. N’oubliez pas que l’ajout de comptes d’ordinateur aux groupes n’est pas recommandé pour deux raisons :

-   Les comptes d’ordinateur sont soumis à la suppression et à la recréation si l’ordinateur quitte le domaine, puis le rejoint.
-   Si vous ajoutez un compte d’ordinateur à un groupe, tous les services qui s’exécutent en tant que LocalSystem sur cet ordinateur sont autorisés à accéder au groupe. Cela est dû au fait que tous les services LocalSystem partagent le compte d’ordinateur de leur serveur hôte. Pour cette raison, il est particulièrement important que les comptes d’ordinateur ne soient pas membres des groupes d’administrateurs de domaine.

Les comptes d’ordinateur ont généralement peu de privilèges et n’appartiennent pas à des groupes. La protection par défaut de la liste de contrôle d’accès dans Active Directory Domain Services autorise un accès minimal pour les comptes d’ordinateur. Par conséquent, les services exécutés en tant que LocalSystem, sur des ordinateurs autres que des contrôleurs de service, n’ont qu’un accès minimal à Active Directory Domain Services.

Si votre service s’exécute sous LocalSystem, vous devez tester votre service sur un serveur membre pour vous assurer que votre service dispose de droits suffisants pour lire/écrire sur les contrôleurs de domaine Active Directory. un contrôleur de domaine ne doit pas être le seul Windows ordinateur sur lequel vous testez votre service. n’oubliez pas qu’un service s’exécutant sous LocalSystem sur un contrôleur de domaine Windows dispose d’un accès complet à Active Directory Domain Services et qu’un serveur membre s’exécute dans le contexte du compte d’ordinateur qui a sensiblement moins de droits.

 

 




