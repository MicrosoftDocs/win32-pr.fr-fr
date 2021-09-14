---
description: Les fonctions d’exportation de l’analyseur fournissent toutes les fonctionnalités des analyseurs dans la DLL de l’analyseur. Chaque DLL de l’analyseur doit implémenter ParserAutoInstallInfo et DllMain. Les fonctions d’exportation restantes doivent être implémentées pour chaque analyseur inclus dans la DLL de l’analyseur.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implémentation des fonctions d’exportation de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b8eafb7e12c36a9413a320652e3d372ffbf51e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009332"
---
# <a name="implementing-parser-export-functions"></a>Implémentation des fonctions d’exportation de l’analyseur

Les fonctions d’exportation de l’analyseur fournissent toutes les fonctionnalités des analyseurs dans la DLL de l’analyseur. Chaque DLL de l’analyseur doit implémenter [**ParserAutoInstallInfo**](parserautoinstallinfo.md) et [**DllMain**](dllmain-parser.md). Les fonctions d’exportation restantes doivent être implémentées pour chaque analyseur inclus dans la DLL de l’analyseur.

Les rubriques suivantes vous montrent comment implémenter les fonctions d’exportation.



| Terme                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implémentation de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Fournit une description et un exemple de code d’implémentation de la fonction [**ParserAutoInstallInfo**](parserautoinstallinfo.md) , qui identifie les analyseurs situés dans une dll de l’analyseur.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implémentation de l’analyseur DllMain](implementing-dllmain-parser.md)<br/>                                    | Fournit une description et un exemple de code d’implémentation de la fonction d' [**analyse DllMain**](dllmain-parser.md) , qui identifie l’existence d’un analyseur, puis libère les ressources que Moniteur réseau utilise pour l’analyseur.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implémentation du Registre](implementing-register.md)<br/>                                                                  | Fournit une description et un exemple de code d’implémentation de la fonction [**Register**](register-parser.md) , qui enregistre toutes les propriétés d’un protocole.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implémentation de RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Fournit une description et un exemple de code d’implémentation de la fonction [**RecognizeFrame**](recognizeframe.md) , qui identifie une instance d’un protocole dans un frame.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implémentation de AttachProperties](implementing-attachproperties.md)<br/>                          | Fournit une description et un exemple de code d’implémentation de la fonction [**AttachProperties**](attachproperties.md) , qui sépare les données que l’analyseur reconnaît, puis joint les descriptions de propriété à chaque propriété de protocole qui existe dans les données reconnues.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implémentation de FormatProperties](implementing-formatproperties.md)<br/>                          | Fournit une description et un exemple de code d’implémentation de la fonction [**FormatProperties**](formatproperties.md) , qui met en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implémentation de l’annulation de l’inscription](implementing-deregister.md)<br/>                                                        | Fournit une description et un exemple de code d’implémentation de la fonction de [**désinscription**](deregister.md) , qui libère les ressources utilisées pour enregistrer les propriétés de protocole.<br/>                                                                                                     |



 

 

 




