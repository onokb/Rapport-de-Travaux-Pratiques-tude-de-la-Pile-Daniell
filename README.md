
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Rapport de TP - Pile Daniell et Oxydoréduction</title>
    <style>
        body { 
            font-family: 'Arial', sans-serif; 
            line-height: 1.6; 
            color: #333333; 
            margin: 0; 
            padding: 40px; 
            background-color: #fafafa; 
        }
        .report-container { 
            max-width: 800px; 
            margin: auto; 
            background: white; 
            padding: 40px; 
            border: 1px solid #e0e0e0; 
            border-radius: 4px; 
        }
        h1 { 
            text-align: center; 
            color: #2c3e50; 
            font-size: 1.6em; 
            border-bottom: 2px solid #2c3e50; 
            padding-bottom: 10px; 
            margin-bottom: 30px; 
        }
        h2 { 
            color: #2980b9; 
            font-size: 1.25em; 
            margin-top: 30px; 
            border-bottom: 1px dashed #ccc;
            padding-bottom: 5px;
        }
        h3 { 
            color: #444; 
            font-size: 1.05em; 
            margin-top: 20px; 
        }
        p { 
            text-align: justify; 
            text-indent: 20px;
        }
        .equation { 
            background: #f8f9fa; 
            border-left: 3px solid #2980b9; 
            padding: 10px; 
            margin: 15px 0; 
            text-align: center; 
            font-family: 'Courier New', Courier, monospace; 
            font-weight: bold; 
        }
        ul { 
            padding-left: 25px; 
        }
        li { 
            margin-bottom: 8px; 
        }
        .schema-box { 
            text-align: center; 
            margin: 30px 0; 
            background: #fdfdfd; 
            border: 1px solid #ddd; 
            padding: 15px; 
        }
        .battery-flex { 
            display: flex; 
            justify-content: center; 
            gap: 50px; 
            margin-top: 20px; 
        }
        .beaker-simple { 
            width: 90px; 
            height: 100px; 
            border: 2px solid #555; 
            border-top: none; 
            border-radius: 0 0 5px 5px; 
            position: relative; 
            background: #ebf5fb;
        }
        .el-zn { background: #95a5a6; width: 15px; height: 110px; position: absolute; top: -20px; left: 35px; }
        .el-cu { background: #dc7633; width: 15px; height: 110px; position: absolute; top: -20px; left: 35px; }
        .bridge-simple { 
            width: 100px; 
            height: 40px; 
            border: 8px solid #bdc3c7; 
            border-bottom: none; 
            position: absolute; 
            margin-left: -50px; 
            margin-top: 20px;
            border-radius: 10px 10px 0 0;
        }
        .caption { 
            font-size: 0.85em; 
            color: #666; 
            margin-top: 15px; 
            font-style: italic; 
        }
        .footer-academic { 
            text-align: center; 
            margin-top: 60px; 
            font-size: 0.8em; 
            color: #3b4445; 
            border-top: 1px solid #868383; 
            padding-top: 15px; 
        }
    </style>
</head>
<body>

    <div class="report-container">
        <h1>Rapport de Travaux Pratiques : Étude de la Pile Daniell</h1>
        
        <h2>1. Introduction et objectif</h2>
        <p>Ce rapport a pour but d'analyser le fonctionnement thermodynamique d'une pile électrochimique spontanée. Le principe de ce dispositif repose sur la conversion directe de l'énergie chimique de réaction (variation d'enthalpie libre &Delta;G) en énergie électrique exploitable under forme de travail (W<sub>e</sub>). Cette transformation est rendue possible par la différence de potentiel standard (E&deg;) entre les deux couples d'oxydoréduction impliqués.</p>

        <h2>2. Description du dispositif expérimental</h2>
        <p>La pile étudiée (modèle Daniell) est constituée de deux demi-piles distinctes, reliées de manière à permettre la circulation des charges tout en évitant le mélange direct des solutions :</p>
        <ul>
            <li><strong>L'anode (pôle négatif) :</strong> Une lame de zinc (Zn) plongée dans une solution de sulfate de zinc. C'est le lieu de l'oxydation.</li>
            <li><strong>La cathode (pôle positif) :</strong> Une lame de cuivre (Cu) plongée dans une solution de sulfate de cuivre, où se produit la réduction.</li>
            <li><strong>Le pont salin :</strong> Un tube contenant une solution gélifiée d'ions inertes (K<sup>+</sup> et Cl<sup>-</sup>) assurant le contact électrique entre les deux compartiments.</li>
        </ul>

        <div class="schema-box">
            <div style="font-weight: bold; color: #555;">Schéma du montage expérimental</div>
            <div style="position: relative; display: inline-block; margin-bottom: 20px;">
                <div class="bridge-simple"></div>
                <div class="battery-flex">
                    <div class="beaker-simple">
                        <div class="el-zn"></div>
                        <span style="position:absolute; bottom:-25px; left:15px; font-size:0.8em;">Anode (Zn)</span>
                    </div>
                    <div class="beaker-simple" style="background: #eaf2f8;">
                        <div class="el-cu"></div>
                        <span style="position:absolute; bottom:-25px; left:12px; font-size:0.8em;">Cathode (Cu)</span>
                    </div>
                </div>
            </div>
            <div class="caption">Figure 1 : Montage de la pile et circulation des porteurs de charge.</div>
        </div>

        <h2>3. Mécanismes de transfert de charge</h2>
        <p>Lorsque le circuit est fermé par une résistance externe, on observe les phénomènes simultanés suivants :</p>
        
        <h3>À l'anode</h3>
        <p>Les atomes de zinc métallique subissent une oxydation et passent en solution sous forme d'ions Zn<sup>2+</sup>, libérant des électrons qui s'accumulent sur l'électrode :</p>
        <div class="equation">Zn (s) = Zn2+ (aq) + 2e-</div>

        <h3>Dans le circuit extérieur</h3>
        <p>Les électrons ne pouvant pas se déplacer dans l'eau, ils traversent le fil conducteur de l'anode vers la cathode. Ce déplacement macroscopique d'électrons crée le courant électrique. Par convention, le courant I circule en sens inverse (du pôle + vers le pôle -).</p>

        <h3>À la cathode</h3>
        <p>Les ions Cu<sup>2+</sup> présents en solution captent les électrons arrivant de l'extérieur pour se réduire en cuivre métallique, qui se dépose sur la lame :</p>
        <div class="equation">Cu2+ (aq) + 2e- = Cu (s)</div>

        <h2>4. Équation bilan et force électromotrice</h2>
        <p>L'équation globale de la réaction d'oxydoréduction s'obtient en sommant les deux demi-réactions :</p>
        <div class="equation">Zn (s) + Cu2+ (aq) &rarr; Zn2+ (aq) + Cu (s)</div>
        
        <p>La force électromotrice (F.E.M.) théorique de la pile dans les conditions standards est déterminée par la relation :</p>
        <div class="equation">E_pile = E&deg;(Cathode) - E&deg;(Anode)</div>

        <h2>5. Rôle du pont salin et neutralité</h2>
        <p>Au fur et à mesure du fonctionnement, le compartiment anodique s'enrichit en ions Zn<sup>2+</sup> (excès de charges positives) tandis que le compartiment cathodique s'appauvrit en ions Cu<sup>2+</sup> (excès de charges négatives dues aux ions sulfates restants). Le pont salin permet de maintenir l'électroneutralité en laissant migrer les ions Cl<sup>-</sup> vers l'anode et K<sup>+</sup> vers la cathode, évitant ainsi le blocage rapide du système par effet coulombien.</p>

        <h2>Conclusion</h2>
        <p>En conclusion, la pile Daniell fonctionne comme un système thermodynamique hors équilibre. Le courant s'arrête lorsque les réactifs sont épuisés. À ce stade, le système atteint son état d'équilibre chimique, l'enthalpie libre devient nulle (&Delta;G = 0) et la tension aux bornes de la pile s'annule (E<sub>pile</sub> = 0 V).</p>

        <div class="footer-academic">
            Compte-rendu de Physique-Chimie • Année Universitaire 2026
        </div>
    </div>

</body>
</html>
