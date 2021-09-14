---
title: Inscription des composants
description: Inscription des composants
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923108"
---
# <a name="registering-components"></a>Inscription des composants

Lorsque les types d’applications suivants sont installés, les informations d’installation doivent être ajoutées au registre, généralement par le biais d’un programme d’installation :

-   Applications serveur
-   Applications conteneur/serveur
-   Applications conteneur qui autorisent la liaison à des objets incorporés

Pour les trois instances, inscrivez les informations de bibliothèque COM (DLL) et les informations spécifiques à l’application.

La DLL enregistre les informations de tous ses composants en exportant [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Utilisez les fonctions suivantes pour inscrire et annuler l’inscription d’un composant :

-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegSetValueEx**](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [**RegEnumKeyEx**](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [**Échec RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> </dl>

 

 