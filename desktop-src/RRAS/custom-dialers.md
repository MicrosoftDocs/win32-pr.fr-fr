---
title: Numéroteurs personnalisés
description: les systèmes d’exploitation Windows 2000 et versions ultérieures permettent aux développeurs de fournir leurs propres numéroteurs personnalisés qui fonctionnent avec le Service d’accès à distance (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Numéroteurs personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791499"
---
# <a name="custom-dialers"></a>Numéroteurs personnalisés

les systèmes d’exploitation Windows 2000 et versions ultérieures permettent aux développeurs de fournir leurs propres numéroteurs personnalisés qui fonctionnent avec le Service d’accès à distance (RAS). Le numéroteur personnalisé est implémenté en tant que bibliothèque de liens dynamiques (DLL) unique qui exporte les points d’entrée suivants :

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

La DLL de numérotation personnalisée doit exporter tous ces points d’entrée et elle doit implémenter les points d’entrée en tant que fonctions Unicode. pour plus d’informations sur ces fonctions, consultez la page de référence de chaque fonction dans le SDK Windows référence du Service d’accès à distance.

Pour qu’une connexion RAS utilise le numéroteur personnalisé, l’entrée de l’annuaire téléphonique pour la connexion doit contenir le chemin d’accès à la DLL de numérotation personnalisée. Utilisez les fonctions d’API RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) et [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir ce chemin d’accès dans le membre **szCustomDialDll** de la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) pour l’entrée de l’annuaire téléphonique.

## <a name="updating-the-registry-for-custom-dialers"></a>Mise à jour du Registre pour les numéroteurs personnalisés

Pour que le système puisse établir une connexion qui utilise un numéroteur personnalisé, le chemin d’accès à la DLL de numérotation personnalisée doit exister dans la valeur de Registre suivante.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Étant donné que **CustomDLL** est de type **reg \_ \_ multisz**, il peut contenir les chemins d’accès à plusieurs dll de numérotation personnalisée. Vous devez définir le chemin d’accès à la DLL de numérotation personnalisée dans cette valeur de Registre, en plus de l’entrée de l’annuaire téléphonique pour la connexion.

Par défaut, cette valeur de Registre est accessible en écriture uniquement par un utilisateur disposant de privilèges d’administrateur ou de système. Pour des raisons de sécurité, ne modifiez pas les autorisations sur cette clé de registre.

## <a name="using-custom-dialers-at-system-logon"></a>Utilisation de numéroteurs personnalisés lors de l’ouverture de session système

les systèmes d’exploitation Windows 2000 et versions ultérieures permettent à un utilisateur d’établir une connexion RAS au moment de l’ouverture de session. Pour ce faire, l’utilisateur vérifie la **connexion à l’aide de l’accès réseau à distance** dans la boîte de dialogue informations de **connexion** . Une fois que l’utilisateur a cliqué sur le bouton OK, le système affiche les connexions disponibles.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Dans la plupart des cas, un numéroteur personnalisé fonctionne avec les privilèges de sécurité de l’utilisateur qui l’appelle. Toutefois, si le numéroteur personnalisé est appelé lors de l’ouverture de session, il fonctionne avec des privilèges système. Par conséquent, concevez le numéroteur personnalisé afin qu’il ne puisse pas être utilisé pour enfreindre la sécurité du système. Par exemple, le numéroteur ne doit pas présenter une interface utilisateur qui permet à l’utilisateur d’écrire un accès au système de fichiers de l’ordinateur. les interfaces utilisateur qui fournissent un tel accès incluent la boîte de dialogue **rechercher un fichier** , la boîte de dialogue commune **ouvrir un fichier** et Windows **aide**.

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>L’interface utilisateur du numéroteur personnalisé doit prendre en charge IDCANCEL

Si le numéroteur personnalisé affiche une interface utilisateur, l’interface utilisateur doit prendre en charge les \_ messages de commande WM où LOWORD (*wParam*) est égal à IDCANCEL.

 

 